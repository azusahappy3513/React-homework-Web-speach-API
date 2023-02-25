# React-homework-Web-speach-API
# 課題　 --

## ①課題内容（どんな作品か）
- 前回までのブック検索にWeb Speach API（音声入力）を追加（する予定でした）
- 時間が来てしまったので一旦提出します。

## ②工夫した点・こだわった

- 1）Web Speach API　で　npm install --save react-speech-recognition でSpeach APIをインストール
　2）以下をBooksCreate.jsx に追記
　　　2－1:import SpeechRecognition, { useSpeechRecognition } from "react-speech-recognition";
　　　2－2：export const BookCreateの中に以下を追記
　const Dictaphone = () => {
  const {
    transcript,
    listening,
    resetTranscript,
    browserSupportsSpeechRecognition,
  } = useSpeechRecognition();

  if (!browserSupportsSpeechRecognition) {
    return <span>Browser doesn't support speech recognition.</span>;
  }　

  3）Returnの戻り値に以下を追記
  <!-- 　 <div>
      <p>Microphone: {listening ? "on" : "off"}</p>
      <button onClick={SpeechRecognition.startListening}>Start</button>
      <button onClick={SpeechRecognition.stopListening}>Stop</button>
      <button onClick={resetTranscript}>Reset</button>
      <p>{transcript}</p>
    </div> -->

## ③難しかった点・次回トライしたいこと(又は機能)
- 動かないｗｗ　エラーがSintax エラーが出るので、); などの部分を調整してみましたがＮＧ．
　ＡＰＩで上記記述した部分を向こうにすると動く。またＡＰＩ単体でも動くぽいです。（ＪＳ）
 　

## ④質問・疑問・感想、シェアしたいこと等なんでも
