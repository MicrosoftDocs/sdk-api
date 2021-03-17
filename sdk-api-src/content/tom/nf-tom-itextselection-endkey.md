---
UID: NF:tom.ITextSelection.EndKey
title: ITextSelection::EndKey (tom.h)
description: Mimics the functionality of the End key.
helpviewer_keywords: ["EndKey","EndKey method [Windows Controls]","EndKey method [Windows Controls]","ITextSelection interface","ITextSelection interface [Windows Controls]","EndKey method","ITextSelection.EndKey","ITextSelection::EndKey","_win32_ITextSelection_EndKey","_win32_ITextSelection_EndKey_cpp","controls.ITextSelection_EndKey","controls._win32_ITextSelection_EndKey","tom/ITextSelection::EndKey","tomColumn","tomLine","tomRow","tomStory"]
old-location: controls\ITextSelection_EndKey.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\endkey.htm
ms.date: 12/05/2018
ms.keywords: EndKey, EndKey method [Windows Controls], EndKey method [Windows Controls],ITextSelection interface, ITextSelection interface [Windows Controls],EndKey method, ITextSelection.EndKey, ITextSelection::EndKey, _win32_ITextSelection_EndKey, _win32_ITextSelection_EndKey_cpp, controls.ITextSelection_EndKey, controls._win32_ITextSelection_EndKey, tom/ITextSelection::EndKey, tomColumn, tomLine, tomRow, tomStory
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextSelection::EndKey
 - tom/ITextSelection::EndKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextSelection.EndKey
---

# ITextSelection::EndKey


## -description

Mimics the functionality of the End key.

## -parameters

### -param Unit

Type: <b>long</b>

Unit to use. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomLine"></a><a id="tomline"></a><a id="TOMLINE"></a><dl>
<dt><b>tomLine</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the end of the last line in the selection. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="tomStory"></a><a id="tomstory"></a><a id="TOMSTORY"></a><dl>
<dt><b>tomStory</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the end of the last line in the story.

</td>
</tr>
<tr>
<td width="40%"><a id="tomColumn"></a><a id="tomcolumn"></a><a id="TOMCOLUMN"></a><dl>
<dt><b>tomColumn</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the end of the last column in the selection. This is available only if the TOM engine supports tables.

</td>
</tr>
<tr>
<td width="40%"><a id="tomRow"></a><a id="tomrow"></a><a id="TOMROW"></a><dl>
<dt><b>tomRow</b></dt>
</dl>
</td>
<td width="60%">
Depending on 
								<i>Extend</i>, it moves either the insertion point or the active end to the end of the last row in the selection. This is available only if the TOM engine supports tables.
						

</td>
</tr>
</table>

### -param Extend

Type: <b>long</b>

Flag that indicates how to change the selection. If 
					<i>Extend</i> is zero (or <b>tomMove</b>), the method collapses the selection to an insertion point. If 
					<i>Extend</i> is 1 (or <b>tomExtend</b>), the method moves the active end and leaves the other end alone. The default value is zero.

### -param pDelta

Type: <b>long*</b>

Pointer to a variable that receives the count of characters that the insertion point or the active end is moved. This parameter can be null.

## -returns

Type: <b>HRESULT</b>

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Unit is neither <b>tomLine</b> nor <b>tomStory</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>

## -remarks

Setting <i>Extend</i> to <b>tomExtend</b> (or nonzero) corresponds to the Shift key being pressed. Setting <i>Unit</i> to <b>tomLine</b> corresponds to the Ctrl key not being pressed.  Setting <i>Unit</i> to <b>tomStory</b> to Ctrl being pressed. The <i>pDelta</i> parameters receives the number of characters that the insertion point or active end is moved.
			

The <a href="/windows/desktop/api/tom/nf-tom-itextselection-homekey">ITextSelection::HomeKey</a> and <b>ITextSelection::EndKey</b> methods are used to mimic the standard Home/End key behavior.

The <b>tomLine</b> value mimics the Home or End key behavior 
				<i>without</i> the Ctrl key pressed, while <b>tomStory</b> mimics the behavior 
				<i>with</i> the Ctrl
				key pressed. Similarly, <b>tomMove</b> mimics the Home or End key behavior 
				<i>without</i> the Shift key pressed, while <b>tomExtend</b> mimics the behavior 
				<i>with</i> the Shift key pressed. So 
				<code>EndKey(tomStory)</code> converts the selection into an insertion point at the end of the associated story, while <code>EndKey(tomStory, tomExtend)</code> moves the active end of the selection to the end of the story and leaves the other end where it was.

The 
				<a href="/windows/desktop/api/tom/nf-tom-itextselection-homekey">HomeKey</a> and <b>EndKey</b> methods are logical methods like the <b>Move*</b> methods, rather than directional methods. Thus, they depend on the language that is involved. For example, in Arabic text, 
				<b>HomeKey</b> moves to the right end of a line, whereas in English text, it moves to the left. Thus, 
				<b>HomeKey</b> and <b>EndKey</b> are different than the <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a> and <a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">MoveRight</a> methods. Also, note that the <b>EndKey</b> method is quite different from the 
				<b>End</b> property, which is the <code>cp</code> at the end of the selection. 
				<b>HomeKey</b> and <b>EndKey</b> also differ from the <a href="/windows/desktop/api/tom/nf-tom-itextrange-startof">StartOf</a> and <a href="/windows/desktop/api/tom/nf-tom-itextrange-endof">EndOf</a> methods in that they extend from the active end, whereas 
				<b>StartOf</b> extends from Start and 
				<b>EndOf</b> extends from End.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-endof">EndOf</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-homekey">HomeKey</a>



<a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-move">Move</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveleft">MoveLeft</a>



<a href="/windows/desktop/api/tom/nf-tom-itextselection-moveright">MoveRight</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-startof">StartOf</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>