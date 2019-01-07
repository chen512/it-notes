<style lang="less">
    .container{
        width:100%;
        overflow:auto;
        //margin:0 auto 2.04rem auto;
    }
    .smallBox {
        height:1rem;
        line-height:normal;
        position:absolute;
        width: 25em;
        word-break:keep-all;
        white-space:nowrap;
        pointer-events: none;
        font-weight: bold;
        //opacity: 0.75;
        font-size: 0.472222rem;
        overflow: hidden;
        color: #fff;
        // text-shadow: -2px 0 #000,2px 0 #000,0 -2px #000,0 2px #000;
        /*-webkit-text-stroke-width:0.018518rem;
        -webkit-text-stroke-color:#000;
        -webkit-text-fill-color: #fff;*/


        text-shadow:#000 0.018518rem 0 0,#000 0 0.018518rem 0,#000 -0.018518rem 0 0,#000 0 -0.018518rem 0;
        -webkit-text-shadow:#000 0.018518rem 0 0,#000 0 0.018518rem 0,#000 -0.018518rem 0 0,#000 0 -0.018518rem 0;
        -moz-text-shadow:#000 0.018518rem 0 0,#000 0 0.018518rem 0,#000 -0.018518rem 0 0,#000 0 -0.018518rem 0;
        *filter: Glow(color=#000, strength=1);
    }

    #videoBox {
        /*height: 25rem;*/
        overflow: hidden;
        // flex-shrink: 0;
        position: relative;
        // width: 100%;
        // height: auto;
    }

    .videoDesc{
        position: absolute;
        top: 1.2rem;
        left: 0.5rem;
        right: 0.5rem;
        font-size: 0.333333rem;
        opacity: 0.9;
    }
    .videoShow{
        display: none;
    }
    .btn-comment{
        position: absolute;
        top: .25rem;
        right: .5rem;
        height: 0.7rem;
        padding-left: 0.5rem;
    }
    .up-btn{
        position: absolute;
        right: 0.5rem;
        top: 2rem;
    }
    .publishTime{
        left: .5rem;
        top: 2.2rem;
        position: absolute;
        opacity: 0.9;
    }
    .playBtn{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
    }
    #videoBox>video {
        width: 100%;
        // height: 100%;
        /*background-color: silver;*/
        /*object-position: 50% 0;*/
        /*object-fit: none;*/
        //object-position: 50% 50%;
        //object-position: 0 50%;
        object-fit: cover;
        // object-position: left top;
        background-color: #000;
    }
    #contentBox {
        overflow: auto;
    }

    #contentBox>ul>li {
        border: 1px solid salmon;
        padding: 10px;
    }

    #contentBox>ul>li>input,
    #contentBox>ul>li>textarea {
        width: 100%;
    }

    #contentBox>ul>li:not(:first-child) {
        border-top-width: 0;
    }

    #videoBox>.floor {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
    }

    #videoBox>.floor>.controls {
        /*position: absolute;*/
        /*bottom: 0;*/
        width: 100%;
        height: 3rem;
        opacity: .5;
        /*line-height: 1rem;*/
        /*font-size: 1rem;*/
        color: white;
        flex-shrink: 0;
        background-image: linear-gradient(-180deg, rgba(0,0,0,0.95) 32%, rgba(67,69,73,0.00) 98%);
    }
    .flex{
        display: flex;
    }
    .conFlex{
        padding: 0.324074rem 0.5rem;

    }
    #videoBox>.floor>.controls-footer {
        /*position: absolute;*/
        /*bottom: 0;*/
        width: 100%;
        height: 3rem;
        opacity: .5;
        display: flex;
        /*line-height: 1rem;*/
        /*font-size: 1rem;*/
        color: #000000;
        flex-shrink: 0;
        background-image: linear-gradient(-180deg, rgba(67,69,73,0.00) 32%, rgba(0,0,0,0.95) 98%);
    }
    /*#videoBox>.floor>.controls>span {
        margin: 0 1rem;
    }*/

    #videoBox>.floor>.controls>span.range {
        flex-grow: 1;
    }

    #videoBox>.floor>.controls>span.range>input {
        width: 100%;
        height: 100%;
    }

    #videoBox>.floor>.barrage_box {
        flex-grow: 1;
    }

    #videoBox>.floor>.barrage_box>.barrage {
        /*display: block;*/
        position: absolute;
        top: 0;
        left: 0;
        color: salmon;
        width: 100%;
        animation: myfirst 5s linear infinite;
        font-size: .472222rem;
    }

    @keyframes myfirst {
        to {
            left: -100%;
            //transform: translateX(-100%);
            /*display: none;*/
        }
    }
    .icon-comment{
        background-image: url(../../assets/images/acgn-share/Icon_Barrage-On.png);
        background-size: 100% auto;
        cursor: default;
        display: inline-block;
        font-family: playerIcons;
        line-height: 0.7rem;
        font-weight: 400;
        font-style: normal;
        -webkit-font-smoothing: antialiased;
        height: 0.7rem;
        background-color: transparent;
        color: #585858;
        width: 0.7rem;
        //margin: 0 0.5rem 0 0;
    }
    .icon-comment-off {
        background-image: url(../../assets/images/acgn-share/Icon_Barrage-Off.png);
    }
    .time{
        margin: 0 0.15rem;
    }
    .fullScreen-icon{
        background-image: url(../../assets/images/acgn-share/Icon_Fullscreen.png);
        background-size: 100% auto;
        cursor: default;
        display: inline-block;
        font-family: playerIcons;
        line-height: 0.7rem;
        font-weight: 400;
        font-style: normal;
        -webkit-font-smoothing: antialiased;
        height: 0.7rem;
        background-color: transparent;
        color: #585858;
        width: 0.7rem;
        margin: 0.15rem auto;
    }
    .up-icon{
        background-image: url(../../assets/images/acgn-share/up.png);
        background-size: 100% 100%;
        cursor: default;
        display: inline-block;
        font-family: playerIcons;
        line-height: 0.444444rem;
        font-weight: 400;
        font-style: normal;
        -webkit-font-smoothing: antialiased;
        height: 0.444444rem;
        background-color: transparent;
        color: #585858;
        width: 0.444444rem;
        margin: 0.15rem auto;
    }
    .play-icon{
        background-size: 100% 100%;
        cursor: default;
        display: inline-block;
        font-family: playerIcons;
        line-height: 1.388888rem;
        font-weight: 400;
        font-style: normal;
        -webkit-font-smoothing: antialiased;
        height: 1.388888rem;
        background-color: transparent;
        color: #585858;
        width: 1.388888rem;
        margin: 0.15rem auto;
    }
    .play-icon-img {
        background-image: url(../../assets/images/acgn-share/play.png);
    }
    .left100{
        left: 100% !important;
    }
    //提示样式
    .tips-mask{
        width:100%;
        height:100%;
        position:fixed;
        top:0;
        left:0;
        background:rgba(0,0,0,0.5);
    }
    .message-tips{
        width:80%;
        max-width:pxToRem(600px);
        position:absolute;
        font-size:pxToRem(32px);
        /*padding:pxToRem(60px) 0;*/
        line-height:pxToRem(40px);
        top:50%;
        left:50%;
        transform: translate(-50%,-50%);
        border-radius:3px;
        text-align:center;
        background:#000;
        background:rgba(0,0,0,0.8);
        box-shadow:0 0 5px rgba(0,0,0,0.5);
        color:#fff;
        &.message-tips--active{
            display:block;
        }
        p{
            padding:0 5%;
            font-size: 0.5rem;
        }
    }
    .download-tips{
        width:100%;
        overflow:hidden;
        position:fixed;
        bottom:0;
        left:0;
        border-top:1px solid #e5e5e5;
        background-color:rgb(255,255,255);
        //z-index: 999;
        padding: 0.166667rem 0.222222rem;
    }
    .download-app__img{
        width: 1rem;
        height: 1rem;
        border-radius: 12px;
        background-color: transparent;
        margin: 0 0.22222rem 0 0;
        float: left;
    }
    .download-app__about{
        display: inline-block;
        margin-top: 0.1rem;
        float:left;
        color: #000;
    }
    .download-app__name{
        height: 0.444rem;
        line-height: 0.444rem;
        font-size: 0.388889rem;
    }
    .download-app__desc{
        margin-top: 0.083333rem;
        line-height: 0.42rem;
        font-size: 0.305556rem;
        opacity: .4;
    }
    .download-link{
        position: absolute;
        top: .35rem;
        width: 1.5rem;
        height: .666667rem;
        font-size: .333333rem;
        border: 1px solid #0AD8F0;
        border-radius: 5rem;
        color: #0AD8F0;
        right: .622222rem;
        margin-top: .00rem;
        /* float: right; */
        text-align: center;
        /* right: 0; */
    }
    .download-link span {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate3d(-50%, -46%, 0);
    }
    .download-tips a {
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>
<template>
<div id="app" class="app">
    <div class="container" id="detailModel">
        <div class="article-content__video">
            <div id="videoBox">
                <video :src="video.url" playsinline webkit-playsinline x5-playsinline x5-video-player-type="h5"
                       x5-video-player-fullscreen="true" x5-video-orientation="landscape|portrait"
                      :poster="videoPoster"></video>
                <div class="floor">
                    <span class="play playBtn"><i class="play-icon play-icon-img"></i></span>
                    <div class="controls">
                        <div class="conFlex flex">
                            <span class="range videoTitle ellipsis">{{title}}</span>
                            <span class="videoDesc videoShow">{{desc}}</span>
                            <span class="publishTime videoShow">{{createTime}}</span>
                            <span class="control-btn up-btn videoShow"><i class="up-icon"></i></span>
                            <span class="control-btn btn-comment active"><i class="player-icon icon-comment"></i></span>
                            <span class="Mute"></span></div>
                    </div>
                    <div class="barrage_box">
                    </div>
                    <div class="controls-footer">
                    </div>
                </div>
            </div>
        </div>
        <!--加载中提示-->
        <div class="detail-loading detail-loading--active" v-if="loadingShow">
            <div class="loadEffect">
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                <span></span>
            </div>
        </div>
        <div class="download-tips" v-cloak>
            <img src="../../assets/images/acgn-share/icon.png" alt="" class="download-app__img">
            <div class="download-app__about">
                <strong class="download-app__name">里世界视频</strong>
                <p class="download-app__desc">二次元短视频App</p>
            </div>
            <div @click="openApp()" class="download-link">
                <span>下载</span>
            </div>
        </div>
        <!--提示弹窗-->
        <div class="tips-mask" v-show="msg!=''" v-cloak>
            <div class="message-tips">
                <p>{{msg}}</p>
            </div>
        </div>
    </div>

</div>
</template>
<script>
    import Vue from 'vue';
    import sha256 from 'sha256'
    import {getDetails, getRecommed, getComment, getDownload} from 'common/api';
    import util from 'common/util';
    export default {
        name: 'App',
        $global: true,
        data: function() {
            return {
                commentList:[],
                commentColor:[],
                commentShow:[],
                pageId:'',
                uid:'',
                title:'',
                createTime:'',
                loadingShow: true,
                url:'',
                video:'',
                videoPoster:'',
                type:'',
                tags:'',
                commentCount:'',
                viewCount:'',
                author: {
                    avatar:'./images/placeholder.png'
                },
                desc:'',
                comment:[],
                msg: '',
                downLoad: {
                    logo: './images/placeholder.png',
                    title: '',
                    desc: '',
                    message: '',
                    isAble: false,
                    url: 'https://videoclips.lishijie.com/f44464e8a75a44e38e272e3faf630ff3/2be455b54f6d4ff891dc2ea2da35507b-83126d9be1df713a4922a21ca95b6653-hd.mp4',
                },
                recommend: [
                ],

            }
        },
        beforeMount() {
            var self = this;
            self.pageId = util.getUrlParam('id'),
            self.uid = util.getUrlParam('uid');
        },
        mounted() {
            var self = this;
            $('video').css({
                //width: window.innerWidth,
                height: innerHeight || clientH,
            });
            self.getDetailData();
            self.getRecommedData();
            self.getCommentData(1);
            // self.getDownload();
            self.$nextTick(function () {
                var userAgent = navigator.userAgent.toLowerCase()
                var isAndroid = /android/i.test(userAgent);
                var danmuSwitch,video = $('video'),
                    videoDesc = $('.videoDesc'),
                    btn_comment= $('.btn-comment'),
                    conFlex = $('.conFlex'),videoTitle=$('.videoTitle'),up_btn=$('.up-btn'),
                    videoTitleup_btn =$('.videoTitle,.up-btn'),videoDescpublishTimeup_btn = $('.videoDesc,.publishTime,.up-btn'),
                    videoDescpublishTime = $('.videoDesc,.publishTime'),
                    icon_comment = $('.icon-comment'),barrage_box = $('.barrage_box'),
                    play_icon = $('.play-icon'),
                    footer = $('.barrage_box,.playBtn,.controls-footer');
                var box = document.getElementsByClassName("barrage_box")[0];
                var clientH = document.documentElement.clientHeight || document.body.clientHeight;
                box.style.height = clientH/108 + "rem";//clientH - 60 px
                if(isAndroid) {
                    video.css({
                        'width': '10rem',
                        'height': innerHeight || clientH
                    })
                }
                var counter = 0;
                var textLs = [];

                function tm(index) {
                    var div = document.createElement("div");
                    div.setAttribute('class', 'smallBox');
                    box.appendChild(div);
                    if(self.commentList[index] != undefined && (textLs.indexOf(self.commentList[index]) < 0)) {
                        textLs.push(self.commentList[index])
                    } else {
                        return;
                    }
                    console.log('index:'+index);
                    div.innerHTML = self.commentList[index] != undefined ? self.commentList[index]:'';
                    div.style.left = "130%";
                    div.style.top = (0 + Math.round(Math.random() * (7)))*7 + '%'
                    var l = div.offsetLeft;
                    var t = div.offsetTop;
                    var time = null;
                    if(counter > self.commentList.length){
                        clearInterval(danmuSwitch);
                        box.hasChildNodes() ? box.removeChild(div) :'';
                    }
                    time = setInterval(function() {
                        l--;
                        if (l < -40) {
                            clearInterval(time);
                            box.hasChildNodes() ? box.removeChild(div) :'';
                        }
                        div.style.left = l + 'px';
                    }, 10)
                }
                //进入全屏状态
                video.on('x5videoenterfullscreen', function() {
                    //延时修改video尺寸以占满全屏
                    //$(this).attr('x5-video-player-type','');
                    setTimeout(function() {
                        video.css({
                            //width: window.innerWidth,
                            height: innerHeight || clientH,
                        });
                    }, 200);
                });
                //退出全屏状态
                video.on('x5videoexitfullscreen', function() {
                    //清除
                    $(this).css({
                        width: '',
                        height: '50%',
                    });
                });
                //更新播放进度
                video.on('timeupdate', function() {
                    var that = this;
                    var len = self.commentShow.length;
                    if(btn_comment.hasClass('active'))
                    for(var i = 0; i < len; i++){
                        (function(i){
                           //console.log('currentTime:'+that.currentTime,'commentShow:'+self.commentShow[i])
                            requestAnimationFrame(function () {
                                //console.log('timeUpdate:'+that.currentTime*1000, self.commentShow[i]);
                                if((that.currentTime*1000-250<= self.commentShow[i])&&(self.commentShow[i]<=that.currentTime*1000+250)){
                                    //console.log('弹幕i:'+i,'弹幕发送时间:'+self.commentShow[i])
                                    tm(i);
                                }
                            })
                        })(i)
                    }
                });
                video.on('canplay',function () {
                    var a = 0;a+=1;
                    console.log('帧:'+a)
                });
                video.on('waiting',function () {
                    var a = 0;a+=1;
                    console.log('waiting:'+a)
                });
                videoTitleup_btn.on('click',function(){
                    if(videoDesc.hasClass('videoShow')){
                        videoDescpublishTimeup_btn.removeClass('videoShow');
                        btn_comment.addClass('videoShow');
                        conFlex.removeClass('flex')
                        videoDescpublishTime.css({position:'relative',left:'0',top:'0',display:'block',marginTop:'0.222222rem'})
                        up_btn.css({position:'relative',display:'block',left:'0',top:'-0.555556rem',float:'right'})
                        videoTitle.removeClass('ellipsis');
                    } else {
                        videoDescpublishTimeup_btn.addClass('videoShow');
                        conFlex.addClass('flex')
                        videoDescpublishTimeup_btn.css({position:'absolute',display:'none'})
                        btn_comment.removeClass('videoShow')
                        videoTitle.addClass('ellipsis');

                    }
                });
                video.on('ended', function() {
                    play_icon.addClass('play-icon-img');
                    textLs = [];
                });
                footer.on('click', function() {
                    if(video[0].paused) {
                        video[0].play();
                        if(!(btn_comment.hasClass('active'))){
                            clearInterval(danmuSwitch)
                        }
                        play_icon.removeClass('play-icon-img')
                    } else {
                        video[0].pause();
                        clearInterval(danmuSwitch)
                        barrage_box.empty();
                        play_icon.addClass('play-icon-img')
                    }
                });
                btn_comment.on('click', function() {
                    if(btn_comment.hasClass('active')){
                        icon_comment.addClass('icon-comment-off');
                        btn_comment.removeClass('active');
                        clearInterval(danmuSwitch)
                        barrage_box.empty();

                    } else {
                        btn_comment.addClass('active');
                        icon_comment.removeClass('icon-comment-off');
                        danmuSwitch =setInterval(tm, 1000);
                    }
                })
            })
        },
        methods: {
            getDetailData(){
                let time = this.getTime();
                let sign = this.getSign([this.pageId,time]);
                let para = {token:this.$store.state.token,sign:sign,ts:time,id:this.pageId,type:2}
                getDetails(para).then((res) => {
                    if(res.status == 200 && res.data.code == 200){
                       this.title = res.data.data.title;
                       this.url = res.data.data.url;
                       this.video = res.data.data.video;
                       this.videoPoster = this.video.image.slice(0,this.video.image.match(/\?/).index) +'?x-oss-process=style/thumbnail_jpg_360';
                       this.desc = res.data.data.desc||'该视频暂无描述！';
                       this.type = res.data.data.type;
                       this.tags = res.data.data.tags;
                       this.commentCount = res.data.data.commentCount;
                       this.viewCount = res.data.data.viewCount;
                       this.author = res.data.data.author;
                    } else {
                        this.msg = res.data.message;
                    }
                },error => {
                    this.msg = '数据异常，请稍后再试';
                }).catch(error=>{
                    this.msg = error.message || '数据异常，请稍后再试';
                });
            },
            getRecommedData(){
                let para = {contentId:this.pageId,imei:86459403005244}
                getRecommed(para).then((res) => {
                    if(res.status == 200 && res.data.code == 200){

                    } else {
                        //this.msg = res.data.message;
                    }
                },error => {
                    this.msg = '数据异常，请稍后再试';
                }).catch(error=>{
                    this.msg = error.message || '数据异常，请稍后再试';
                });
            },
            getCommentData(n){
                let time = this.getTime();
                let sign = this.getSign([this.pageId,n,time]);
                let para = {token:'',sign:sign,ts:time,contentId:this.pageId,page:1}
                getComment(para).then((res) => {
                    if(res.status == 200 && res.data.code == 200){
                        var data = res.data.data;
                        data.forEach(item => {
                            item.border = 'border' + parseInt(Math.random()*8);
                        })
                        data = data.map(item =>{
                            item.avatar = /image\.lishijie/.test(item.avatar) ? item.avatar.slice(0,item.avatar.match(/\?/) && item.avatar.match(/\?/).index) + '?x-oss-process=style/thumbnail_jpg_360' : (item.avatar ? item.avatar : 'https://activity.lishijie.com/publicImg/bgavatar.png')
                            return item;
                        })
                        this.comment = data;
                        this.commentList = this.comment.map(item=> item.content);
                        this.commentColor = this.comment.map(item=> item.timeline.split(',')[3]);
                        this.commentShow = this.comment.map(item=> item.timeline.split(',')[0]);
                    } else {
                        //this.msg = res.data.message;
                    }
                },error => {
                    this.msg = '数据异常，请稍后再试';
                }).catch(error=>{
                    this.msg = error.message || '数据异常，请稍后再试';
                });
            },
            getDownload(){
                let time = this.getTime();
                let sign = this.getSign([time]);
                let para = {token:'',sign:sign,ts:time,uid:this.uid};
                getDownload(para).then((res) => {
                    if(res.status == 200 && res.data.code == 200){
                    this.downLoad = {
                            logo:res.data.data.logo,
                            title:res.data.data.title,
                            desc:res.data.data.desc,
                            message:res.data.data.download.message,
                            isAble:res.data.data.download.isEnableDownload==='false' ? false : true,
                            url:res.data.data.download.url
                        }
                    } else {
                        //this.msg = res.data.message;
                    }
                },error => {
                    this.msg = '数据异常，请稍后再试';
                }).catch(error=>{
                    this.msg = error.message || '数据异常，请稍后再试';
                });
            },
            getSign(arr){
                return sha256(arr.join(''));
            },
            getTime(){
                return new Date().getTime();
            },
            openApp() {
                let url = {};
                let ua = navigator.userAgent.toLowerCase();
                if(ua.match(/iphone|ipod|ipad/)){
                    this.msg = 'iOS版本即将上线，敬请期待';
                    setTimeout(() => {
                        this.msg = '';
                    }, 1000);
                    return
                }
                if(ua.match(/android/i)){
                    url = {
                        // open: 'lishijie://splash/splash',
                        open: 'acg://com.lishijie.acg.video/main',
                        down: 'https://www.lishijie.net/download/android/short_video/lishijie.apk',
                        store: 'market://search?q=里世界视频'
                    };
                }
                let winScreenWidth = window.screen.width;
                if((/MicroMessenger/gi.test(navigator.userAgent) || ua.match(/WeiBo/i) == "weibo") && ua.match(/android/i)) {
                    // todo 更改包名
                    window.location.href = 'http://a.app.qq.com/o/simple.jsp?pkgname=com.lishijie.acg.video';
                   // this.msg = '请前往浏览器打开该页面';
                    /*setTimeout(() => {
                        this.msg = '';
                    }, 1000);*/
                } else if(winScreenWidth < 800){
                    let iframe = document.createElement('iframe');
                    let isInstalled = false;
                    let timer = null;
                    document.body.appendChild(iframe);
                    iframe.src = url.open;
                    iframe.style.display = 'none';
                    iframe.onload = function(e){
                        var e = e || window.event;
                        e.preventDefault();
                        isInstalled = true;
                    }
                    iframe.onerror = function() {
                        isInstalled = false;
                    }
                    timer = setTimeout(function() {
                        document.body.removeChild(iframe);
                        window.location.href = url.down;
                    }, 2000);
                } else {
                    window.location.href = 'https://www.lishijie.net/download/android/short_video/lishijie.apk'
                }
            },
        },
        components: {}
    }
</script>
