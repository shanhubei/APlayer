# 歌词

## LRC 格式

```
[ti:歌词(歌曲)的标题]
[al:本歌所在的唱片集]
[ar:演出者-歌手]
[au:歌词作者-作曲家]
[by:此LRC文件的创建者]
[offset:+/- 以毫秒为单位加快或延后歌词的播放]

[re:创建此LRC文件的播放器或编辑器]
[ve:程序的版本]

[mm:ss.ms] 我们一起学猫叫
[mm:ss.ms][mm:ss:ms] 一起喵喵喵喵喵
...
```

查看维基百科了解更多：<https://zh.wikipedia.org/wiki/LRC%E6%A0%BC%E5%BC%8F>

## LRC 文件

<aplayer-lrc lrc="https://cdn.moefe.org/music/lrc/kiss.lrc" :lrcType="3" />

📝 example.vue

```vue
<template>
  <!--
    指定 lrcType 为 3，表示 audio.lrc 的值是 lrc 文件地址，
    将通过 `fetch` 获取 lrc 歌词文本。
  -->
  <aplayer audio=":audio" :lrcType="3" />
</template>

<script>
import Vue from 'vue';
import APlayer from '@moefe/vue-aplayer';

Vue.use(APlayer);

export default {
  data() {
    return {
      audio: {
        name: '啵唧',
        artist: 'Hanser',
        url: 'https://cdn.moefe.org/music/mp3/kiss.mp3',
        cover: 'https://p1.music.126.net/K0-IPcIQ9QFvA0jXTBqoWQ==/109951163636756693.jpg?param=300y300', // prettier-ignore
        lrc: 'https://cdn.moefe.org/music/lrc/kiss.lrc',
      },
    };
  },
};
</script>
```

## LRC 字符串

<aplayer-lrc lrc="[00:00.00] 我们一起学猫叫\n[99:99.99] 一起喵喵喵喵喵" :lrcType="1" />

📝 example.vue

```vue
<template>
  <!-- 指定 lrcType 为 1，表示 audio.lrc 的值是 lrc 字符串 -->
  <aplayer :audio="audio" :lrcType="1" />
</template>

<script>
import Vue from 'vue';
import APlayer from '@moefe/vue-aplayer';

Vue.use(APlayer);

export default {
  data() {
    return {
      audio: {
        name: '啵唧',
        artist: 'Hanser',
        url: 'https://cdn.moefe.org/music/mp3/kiss.mp3',
        cover: 'https://p1.music.126.net/K0-IPcIQ9QFvA0jXTBqoWQ==/109951163636756693.jpg?param=300y300', // prettier-ignore
        lrc: '[00:00.00] 我们一起学猫叫\n[99:99.99] 一起喵喵喵喵喵',
      },
    };
  },
};
</script>
```

## 禁用歌词

<aplayer-lrc :lrcType="0" />

📝 example.vue

```vue
<template>
  <!-- 指定 lrcType 为 0，表示禁用歌词 -->
  <aplayer :audio="audio" :lrcType="0" />
</template>

<script>
import Vue from 'vue';
import APlayer from '@moefe/vue-aplayer';

Vue.use(APlayer);

export default {
  data() {
    return {
      audio: {
        name: '啵唧',
        artist: 'Hanser',
        url: 'https://cdn.moefe.org/music/mp3/kiss.mp3',
        cover: 'https://p1.music.126.net/K0-IPcIQ9QFvA0jXTBqoWQ==/109951163636756693.jpg?param=300y300' // prettier-ignore
      },
    };
  },
};
</script>
```
