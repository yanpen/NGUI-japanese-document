===============
12.Chat Window
===============

.. This example shows how to create a simple chat window. A chat window is made up of two main components:
このExampleでは、単純なチャットウィンドウを作成する方法を示します。チャットウィンドウは2つの主要コンポーネントで構成されています。

.. The Input field where a user can type something.
1. ユーザーが何かを入力することができます入力フィールド。

.. An area with text.
2. テキストとエリア。

.. Input field is easy, and is covered in the 7th Tutorial, but the text area? Equally simple, actually: UITextList. This script allows you to dynamically create text lines and arrange them in either the Text Style (scroll position of 0 being the top), or the Chat Style (scroll position of 0 being on the bottom).
入力フィールドは簡単で、7番目のチュートリアルでカバーされていますが、テキストエリアですか？同様にシンプルです、実際に： **UITextList** です。このスクリプトでは、動的にテキスト行を作成し、 ``TextStyle`` （ ``scroll`` の ``position`` が ``0`` はトップ）、または ``Chat Style`` （  ``scroll`` の ``position`` が ``0`` はボトム）でそれらをアレンジすることができます。

.. Now, I should probably mention that this script does not actually create any labels. It simply works with an existing label you specify and fills its contents using its own list of text entries and the current scroll value. You can also specify the size of the text area as well as the maximum number of paragraphs before they start getting recycled (with the oldest one being reused to create the latest).
今、おそらくこのスクリプトは実際に任意のラベルを作成 **しない** ことに言及する必要があります。それは単にあなたが指定した既存のラベルで動作し、そのテキストエントリの独自のリストと現在の ``scroll`` を使用して、その内容を埋めます。また、テキストエリアの大きさだけでなく、それらがリサイクルの取得を開始する前に段落の最大数を指定することができます（最新を作成するために再利用されている最古のものを含む）。

.. The scrolling is accomplished by another feature built into UITextList, but can be turned off via a checkbox on the script.
スクロールは **UITextList** に組み込まれた別の機能によって達成されていますが、スクリプトのチェックボックスを経由してオフにすることができます。

.. Last but not least, the actual input activation is handled via ChatInput — a custom script written for this example. It’s pretty short, only 70 lines — and all it does inside is:
最後になりましたが、実際の入力のアクティブ化は、 **ChatInput** を介して処理されます - このExampleのためにカスタムスクリプトが書かれています。それは、わずか70行のかなり短いです - すべては内部にあります：

.. Populates the Text List with some dummy data on Start().
1. **Start()** 上でいくつかのダミーデータを使用して **Text List** をに集めます。

.. Selects the input if the Enter key gets pressed.
2. **Enter** キーが押された場合は、 **Enter** を選択します。

.. Calls UITextList.Add with the input field’s text when OnSubmit() message is received (sent by the Input Field), then clears the input field’s text.
3. **OnSubmit()** メソッドメッセージ（入力フィールドで送信された）受信される入力フィールドのテキストを **UITextList.Add** のコールすることで、入力フィールドのテキストをクリアします。

.. End result? Fully functional (albeit a little ugly) chat window that will work on all devices.
最終結果ですか？すべてのデバイス上で動作する（少し醜いとはいえ）チャットウィンドウは完全に機能します。

.. image:: ../images/example4.jpeg

