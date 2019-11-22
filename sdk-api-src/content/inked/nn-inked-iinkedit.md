---
UID: NN:inked.IInkEdit
title: IInkEdit (inked.h)

description: "."
old-location: tablet\iinkedit_.htm
tech.root: tablet
ms.assetid: 8F47529B-52E9-4D67-81B3-DD2584B98101

ms.date: 12/05/2018
ms.keywords: IInkEdit, IInkEdit interface [Tablet PC], IInkEdit interface [Tablet PC],described, inked/IInkEdit, tablet.iinkedit_
ms.topic: interface
f1_keywords: 
 - "inked/IInkEdit"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkEdit</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkEdit</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-change">Change</a>
</td>
<td align="left" width="63%">
Occurs when the content of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-click">Click</a>
</td>
<td align="left" width="63%">
Occurs when a user clicks the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-dblclick">DblClick</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is double-clicked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-gesture">Gesture</a>
</td>
<td align="left" width="63%">
Occurs when an application gesture  is recognized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-keydown">KeyDown</a>
</td>
<td align="left" width="63%">
Occurs when the user presses a key while the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-keypress">KeyPress</a>
</td>
<td align="left" width="63%">
Occurs when the user presses and releases a key while the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-keyup">KeyUp</a>
</td>
<td align="left" width="63%">
Occurs when the user releases a key while the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control has focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-mousedown">MouseDown</a>
</td>
<td align="left" width="63%">
Occurs when the user presses a mouse button while the mouse is over the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-mousemove">MouseMove</a>
</td>
<td align="left" width="63%">
Occurs when the user moves the mouse while the mouse is over the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-mouseup">MouseUp</a>
</td>
<td align="left" width="63%">
Occurs when the user releases a mouse button while the mouse is over the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-recognitionresult">RecognitionResult</a>
</td>
<td align="left" width="63%">
Occurs when the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control gets results manually from a call to the <a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-recognize">InkEdit::Recognize</a> method or automatically after the recognition timeout fires.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-selchange">SelChange</a>
</td>
<td align="left" width="63%">
Occurs when the current selection of text in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control has changed or the insertion point has moved.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-stroke">Stroke</a>
</td>
<td align="left" width="63%">
Occurs when the user draws a new <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object on any <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet</a> object.

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
<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-getgesturestatus">GetGestureStatus</a>
</td>
<td align="left" width="63%">
Indicates whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is interested in a particular application gesture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-recognize">Recognize</a>
</td>
<td align="left" width="63%">
Performs recognition on an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and returns recognition results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Causes the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control to redraw.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus">SetGestureStatus</a>
</td>
<td align="left" width="63%">
Modifies the interest of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control in a known application gesture.

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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance">Appearance</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines the appearance of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control - whether it is flat (painted with no visual effects) or 3D (painted with three-dimensional effects).


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor">BackColor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the background color for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle">BorderStyle</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control has a border.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll">DisableNoScroll</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether scroll bars in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control are disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes">DrawingAttributes</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets or sets the drawing attributes for ink that is yet to be drawn on the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that determines whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control can respond to user-generated events.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid">Factoid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/tablet/factoid-constants">Factoid</a> constant that a <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object uses to constrain its search for the recognition result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_font">Font</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd">Hwnd</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a handle to the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode">InkInsertMode</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies how ink is inserted onto the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control, either as text or as ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode">InkMode</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_locked">Locked</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value indicating whether the contents of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control can be edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength">MaxLength</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Gets or sets a value indicating whether there is a maximum number of characters an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control can hold and, if so, specifies the maximum number of characters.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon">MouseIcon</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the custom mouse icon for the
<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer">MousePointer</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline">MultiLine</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
 Gets or sets a value indicating whether an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control can accept and display multiple lines of text.


</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout">RecognitionTimeout</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the length of time, in milliseconds, between the last <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp">IInkStrokeDisp</a> object collected and the beginning of text recognition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer">Recognizer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer</a> object to use for recognition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars">ScrollBars</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the type of scroll bars, if any, to display in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment">SelAlignment</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that controls the alignment of the paragraphs in an <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold">SelBold</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset">SelCharOffset</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Returns or sets a value that determines whether text in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control appears on the baseline (normal), as a superscript above the baseline, or as a subscript below the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor">SelColor</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname">SelFontName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize">SelFontSize</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks">SelInks</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the array of embedded <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp</a> objects (if displayed as ink) in the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode">SelInksDisplayMode</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic">SelItalic</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control is italic (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength">SelLength</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the number of characters that are selected in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf">SelRTF</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the currently selected Rich Text Format (RTF) formatted text in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart">SelStart</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the starting point of the text that is selected in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext">SelText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the selected text within the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline">SelUnderline</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that specifies whether the font style of the currently selected text in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control is underlined (run time only).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_status">Status</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a value that specifies whether the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a> control is idle, collecting ink, or recognizing ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_text">Text</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the current text in the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf">TextRTF</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the text of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control">InkEdit</a> control, including all RTF codes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput">UseMouseForInput</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates whether the mouse can be used as an input device.

</td>
</tr>
</table> 

