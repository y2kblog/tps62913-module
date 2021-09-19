# TPS62913 低ノイズ・低リップル 可変出力降圧モジュール
<!-- # TPS62913 低ノイズ・低リップル可変出力降圧モジュール -->

<img src="/img/ProductImage_BothSide.jpg" width="350px">

## 概要

低ノイズ・低リップルの降圧型DC/DCコンバータ TPS62913 (Texas Instruments Inc.製) を搭載したモジュールです。  
低ノイズLDOに匹敵する**20µV<sub>RMS</sub>の1/fノイズ**と、IC内蔵のフェライトビーズLCフィルタ補償機能による**10µV<sub>RMS</sub>未満の低リップル**を実現しており、ノイズの影響を受けやすいアプリケーション（例：実験用精密電源、高速ADC、レーダー）の電源供給に最適です。  
また、スイッチングレギュレータのため最大3.0Aの電流を出力できます。  
<!--内部基準電圧のフィルタ処理により-->

### 仕様
- 入力電圧：3.0～17.0V
- 出力電圧：0.9～5.2V (基板上の半固定抵抗で調整)
- 最大出力電流：3.0A
- 1/fノイズ：20µV<sub>RMS</sub> (100Hz～100kHz)
- 電圧リップル：10µV<sub>RMS</sub>未満 (typ.)
- イネーブルピン付き
- パワー・グッドピン付き
- 出力放電機能：有効
- ソフトスタート時間：10.7ms (typ.)
- 基板サイズ：20mm × 22mm
- ピン間隔：2.54mm
<!--
- スイッチング周波数：2.2MHz (typ.)
- スペクトラム拡散変調：有効
-->

<!--
## 販売  
[スイッチサイエンス委託販売ページ](https://www.switch-science.com/catalog/xxxx/)  
※大量注文や在庫に関する問い合わせは[こちら](mailto:info.y2kb@gmail.com)までご連絡ください。  
-->

## ピンアサイン
<table>
    <tbody>
        <tr>
            <td>1</td>
            <td>VIN</td>
            <td>電源入力</td>
        </tr>
        <tr>
            <td>2</td>
            <td>GND</td>
            <td>グラウンド（基準電位）</td>
        </tr>
        <tr>
            <td>3</td>
            <td>VOUT</td>
            <td>電源出力</td>
        </tr>
        <tr>
            <td>4</td>
            <td>EN</td>
            <td>イネーブル<br>デフォルトではENピンはVINピンに基板内部で接続されており、常時出力ONです。基板裏面のJP1ショートジャンパをカッター等で切断するとENピンによる出力ON/OFF制御が可能になり、ENピンに約1V以上を印加すると出力がONになります。</td>
        </tr>
        <tr>
            <td>5</td>
            <td>PG</td>
            <td>パワー・グッド<br>VOUTが設定電圧の約95%を上回るとGNDと同等の電圧となります。約90%を下回るとVOUTと同等の電圧となります。</td>
        </tr>
    </tbody>
</table>

## 回路図  
<img src="/img/schematic.png" width="800px">  

<!--<a href="/hardware/tps62913-module.pdf">回路図(PDF)</a>  -->

## 基板寸法
<img src="/img/dimension.png" width="350px">

## 資料
- 2Dデータ(DXF)：<a href="https://github.com/y2kblog/tps62913-module/raw/master/hardware/dxf/tps62913-module_dxf.zip" download="">tps62913-module_dxf.zip</a>  
- 3Dデータ(STEP)：<a href="https://github.com/y2kblog/tps62913-module/raw/master/hardware/step/tps62913-module_step.zip" download="">tps62913-module_step.zip</a>  
- [TPS61099xデータシート](https://www.tij.co.jp/lit/gpn/tps62913)

## License
MIT License, see `/LICENSE`.
