<template>
  <div class="messageBox">
      <h2>{{title}}</h2>
      <p>{{content}}</p>
      <div>
          <div @touchstart="handleCancel" >{{cancel}}</div>
          <div @touchstart="handleOk">{{ok}}</div>
      </div>
  </div>
</template>

<script>
export default {
    name:'MessageBox',
    
}
</script>

<style>
.messageBox{
    width: 200px;
    height: 120px;
    border: 1px solid rgb(201, 201, 201);
    border-radius: 4px;
    background: white;
    box-shadow: 3px 3px 3px 3px #ccc;
    position: absolute;
    left: 50%;
    top: 50%;
    margin: -60px 0 0 -100px;
}
.messageBox h2{
    text-align: center;
    line-height: 40px;
    font-size: 18px;
}
.messageBox p{
        text-align: center;
    line-height: 40px;
}
.messageBox>div{
    display: flex;
    position: absolute;
    bottom: 0;
    width: 100%;
    border-top: 1px solid rgb(202, 202, 202);

}
.messageBox>div div{
    flex: 1;
    text-align: center;
    line-height: 30px;
    border-right: 1px solid rgb(221, 221, 221);
}
.messageBox>div div:last-child{
    border: none;
}
</style>