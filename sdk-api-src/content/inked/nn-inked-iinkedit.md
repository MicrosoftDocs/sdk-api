---
UID: NN:inked.IInkEdit
title: IInkEdit
author: windows-sdk-content
description: "."
old-location: tablet\iinkedit_.htm
tech.root: tablet
ms.assetid: 8F47529B-52E9-4D67-81B3-DD2584B98101
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IInkEdit, IInkEdit interface [Tablet PC], IInkEdit interface [Tablet PC],described, inked/IInkEdit, tablet.iinkedit_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inked.h
api_name:
 - IInkEdit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkEdit interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkEdit</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkEdit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Events</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkEdit</b> interface has these events.
<table class="members" id="memberListEvents">
<tr>
<th align="left" width="37%">Event</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c65fcca-c84a-414c-a4e5-c5fdffb13e51">Change</a>
</td>
<td align="left" width="63%">
Occurs when the content of the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99fd7ef0-02cf-4390-9026-00ef2bbc1e37">Click</a>
</td>
<td align="left" width="63%">
Occurs when a user clicks the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/380499e4-8697-4823-8153-29f24b2f234c">DblClick</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control is double-clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/736715f4-c610-42cc-9fbb-c2b579da69e5">Gesture</a>
</td>
<td align="left" width="63%">
Occurs when an application gesture  is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14b05b72-ae5d-416a-8ea5-9d9716c0967f">KeyDown</a>
</td>
<td align="left" width="63%">
Occurs when the user presses a key while the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8284ab41-dfac-4da2-b101-6968a43b15d7">KeyPress</a>
</td>
<td align="left" width="63%">
Occurs when the user presses and releases a key while the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/973d99f2-df09-4315-aaab-72877272100b">KeyUp</a>
</td>
<td align="left" width="63%">
Occurs when the user releases a key while the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8985fee5-7b63-46ab-b229-046e2f0ee004">MouseDown</a>
</td>
<td align="left" width="63%">
Occurs when the user presses a mouse button while the mouse is over the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ccaf2eb-acec-4dfd-9ec7-c78aca043900">MouseMove</a>
</td>
<td align="left" width="63%">
Occurs when the user moves the mouse while the mouse is over the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c9e0229-c7e2-4b5c-9532-18fbf8a3667d">MouseUp</a>
</td>
<td align="left" width="63%">
Occurs when the user releases a mouse button while the mouse is over the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09618be0-fe49-494f-940f-79ff8352097e">RecognitionResult</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control gets results manually from a call to the <a href="https://msdn.microsoft.com/e22043da-6c38-49e2-9651-43211ce7f377">InkEdit::Recognize</a> method or automatically after the recognition timeout fires.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14ddffe7-bdfe-4a35-82c7-b3401b5b720c">SelChange</a>
</td>
<td align="left" width="63%">
Occurs when the current selection of text in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control has changed or the insertion point has moved.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fac5104d-d0da-40b1-a4a6-00a34718d09f">Stroke</a>
</td>
<td align="left" width="63%">
Occurs when the user draws a new <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object on any <a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet</a> object.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>IInkEdit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0992dbd2-bd32-4af6-abd1-66027dd2b30f">GetGestureStatus</a>
</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control is interested in a particular application gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e22043da-6c38-49e2-9651-43211ce7f377">Recognize</a>
</td>
<td align="left" width="63%">
Performs recognition on an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection and returns recognition results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74b8e3dc-7bea-4188-bd0d-681e4661828c">Refresh</a>
</td>
<td align="left" width="63%">
Causes the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control to redraw.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fc9daa5-ee34-409b-b977-0d39b23d422e">SetGestureStatus</a>
</td>
<td align="left" width="63%">
Modifies the interest of the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control in a known application gesture.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkEdit</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4575728c-79ca-4b3f-b068-3b0f8f976cf9">Appearance</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines the appearance of the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control - whether it is flat (painted with no visual effects) or 3D (painted with three-dimensional effects).


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/95156660-3d99-4628-aaae-b4d95e4fa6d1">BackColor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the background color for the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/89d42f9c-6354-4159-9717-23c6484b10af">BorderStyle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control has a border.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/44a8372c-6323-4d76-9038-d61d210990b0">DisableNoScroll</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether scroll bars in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control are disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8f5f00a2-abe1-487e-a067-2b6d929824c7">DrawingAttributes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the drawing attributes for ink that is yet to be drawn on the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e3a143ed-82e4-46ba-9745-066eaa08bf7f">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control can respond to user-generated events.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/150325e4-dd8b-4abf-baa6-f0fda05d2fd9">Factoid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">Factoid</a> constant that a <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object uses to constrain its search for the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/af8234bb-7d53-45c7-9edc-fd4e6b64eed3">Font</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a Font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e2f01318-5073-43d2-9d26-91aeef5d7070">Hwnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a handle to the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6fcc119d-45b1-47d3-98eb-4eb04fccfb61">InkInsertMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies how ink is inserted onto the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control, either as text or as ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0e395907-108b-40cf-819b-65a34e4ffc4d">InkMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether ink collection is disabled, ink is collected, or ink and gestures are collected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/67488146-b2ca-484a-b9e5-e2a8c9519d69">Locked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value indicating whether the contents of the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/603074d4-3222-4593-a5e8-b5f8a8dced6a">MaxLength</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Gets or sets a value indicating whether there is a maximum number of characters an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control can hold and, if so, specifies the maximum number of characters.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/11e7cf2d-e671-471f-9a13-1f55b62b4dfa">MouseIcon</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the custom mouse icon for the
<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a5d9a6cc-d777-4619-b28b-17cc79584171">MousePointer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value indicating the type of mouse pointer to be displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/361cfaea-d961-423c-98b0-f04bd7e621e9">MultiLine</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Gets or sets a value indicating whether an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control can accept and display multiple lines of text.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e1171aa3-841f-433e-88b8-e3fc63129aeb">RecognitionTimeout</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the length of time, in milliseconds, between the last <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object collected and the beginning of text recognition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/531bc7f0-1a62-40c2-81f9-ceafe9388a0e">Recognizer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a> object to use for recognition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d6b798dc-6e8f-4c89-b5a8-c4a189ebe6cd">ScrollBars</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the type of scroll bars, if any, to display in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/62755220-b8e4-4f26-b5f4-8a1b4b7adc01">SelAlignment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that controls the alignment of the paragraphs in an <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/423f9303-38e9-4d70-88cd-e6503a9f0a64">SelBold</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control is bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/535224ff-0b91-4814-8100-b6a52afee370">SelCharOffset</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Returns or sets a value that determines whether text in the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control appears on the baseline (normal), as a superscript above the baseline, or as a subscript below the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/06a4ed72-e2c2-4422-8796-39a65b19415e">SelColor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the text color of the current text selection or insertion point (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2aa1e53b-75cc-412d-b522-2e1c91ce31d3">SelFontName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the font name of the selected text within the InkEdit control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a6e3de31-e821-4f14-a3ec-f4ea0ed6f339">SelFontSize</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the font size of the selected text within the InkEdit control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dbdd590d-a8d8-44e9-aecc-fbbe0d24ea20">SelInks</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the array of embedded <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> objects (if displayed as ink) in the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c4e6f85a-b776-41ca-bfd2-6eb8d2425cd1">SelInksDisplayMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that allows for toggling the appearance of the selection between ink and text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ea6f6495-d740-4aad-8310-7ce43f36cd93">SelItalic</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control is italic (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6295a536-831e-4603-9412-87b2fa5b7f53">SelLength</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the number of characters that are selected in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/85dc3b6d-54fa-4f23-9d36-03becff886cf">SelRTF</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the currently selected Rich Text Format (RTF) formatted text in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5f8925c0-ec62-425e-a020-9c534056e63f">SelStart</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the starting point of the text that is selected in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2cd805b5-f421-48d1-9678-b3cae0bc6b86">SelText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the selected text within the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1df7d95c-9f54-4ceb-a4c8-a1c9fbebf714">SelUnderline</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control is underlined (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/47a41d5c-2598-4dfc-a5b5-af4df7fdaa6d">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that specifies whether the <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control is idle, collecting ink, or recognizing ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1b0b2354-7aa5-4e3f-8f7f-9e613c923f9f">Text</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the current text in the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7819d1eb-03b3-407f-a50f-2f7dc7eb474a">TextRTF</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the text of the <a href="https://msdn.microsoft.com/a1dfa254-cade-44c5-8fdd-74bb40849063">InkEdit</a> control, including all RTF codes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e4a425db-6a81-494d-818f-50a53d8c124b">UseMouseForInput</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates whether the mouse can be used as an input device.

</td>
</tr>
</table> 

