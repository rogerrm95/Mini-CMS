<template>
   <div class="stat">
       <div class="stat-icon">
           <i :class="icon" :style="style"></i>
       </div>

       <div class="stat-info">
           <span class="stat-title">{{title}}</span>
           <span class="stat-value">{{value}}</span>
        </div>
   </div>
</template>

<script>
export default {
    name: 'Stat',
    props: ['title', 'value','icon','color'],
    computed:{
        style(){
            return "color:" + (this.color || 'black')
        }
    }
}
</script>

<style>

.stat{
    flex:1;

    display: flex;
    border-radius: 4px;
    margin-bottom: 20px;
    margin-right: 20px;
    background-color: white;
    padding: 20px;
    border:1px solid rgba(0,0,0,0.15);
    box-shadow: 0px 8px 10px rgba(0,0,0,0.15);
}

.stat-icon{
    align-items: center;
    display: flex;

}

.stat-icon > i{
    font-size: 5rem;
}

.stat-info{
    flex:1;
    display: flex;
    flex-direction: column;
    justify-items: flex-end;
    align-items: flex-end;
    padding-bottom: 10px; 
}

.stat-title{
    font-size: 1.2rem;
}

.stat-value{
    font-size: 2rem;
}


</style>