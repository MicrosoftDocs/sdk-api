---
UID: NF:uiautomationcore.ITextRangeProvider.Move
title: ITextRangeProvider::Move (uiautomationcore.h)
description: Moves the text range forward or backward by the specified number of text units.
helpviewer_keywords: ["ITextRangeProvider interface [Windows Accessibility]","Move method","ITextRangeProvider.Move","ITextRangeProvider::Move","Move","Move method [Windows Accessibility]","Move method [Windows Accessibility]","ITextRangeProvider interface","uiauto.uiauto_ITextRangeProvider_Move","uiauto_ITextRangeProvider_Move","uiautomationcore/ITextRangeProvider::Move","winauto.uiauto_ITextRangeProvider_Move"]
old-location: winauto\uiauto_ITextRangeProvider_Move.htm
tech.root: WinAuto
ms.assetid: 09cd8826-4fdf-4ea5-8159-18bb81e3b5cf
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],Move method, ITextRangeProvider.Move, ITextRangeProvider::Move, Move, Move method [Windows Accessibility], Move method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_Move, uiauto_ITextRangeProvider_Move, uiautomationcore/ITextRangeProvider::Move, winauto.uiauto_ITextRangeProvider_Move
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRangeProvider::Move
 - uiautomationcore/ITextRangeProvider::Move
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider.Move
---

# ITextRangeProvider::Move


## -description

Moves the text range forward or backward by the specified number of text units.

## -parameters

### -param unit [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

The type of text units, such as character, word, paragraph, and so on.

### -param count [in]

Type: <b>int</b>

The number of text units to move. A positive value moves the text range forward. 

A negative value moves the text range backward. Zero has no effect.

### -param pRetVal [out, retval]

Type: <b>int*</b>

The number of text units actually moved. This can be less than the number requested if either of the new text range endpoints is greater than or less than the endpoints retrieved by the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-get_documentrange">ITextProvider::DocumentRange</a> method. This value can be negative if navigation is happening in the backward direction.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>ITextRangeProvider::Move</b> should only move the text range to span a different part of the text, it should not alter the text in any way.

            
            

For a non-degenerate (non-empty) text range, <b>ITextRangeProvider::Move</b> should normalize and move the text range by performing the following steps.
            

<ol>
<li>Collapse the text range to a degenerate (empty) range at the starting endpoint.</li>
<li>If necessary, move the resulting text range backward in the document to the beginning of the requested unit boundary.</li>
<li>Move the text range forward or backward in the document by the requested number of text unit boundaries.</li>
<li>Expand the text range from the degenerate state by moving the ending endpoint forward by one requested text unit boundary. </li>
</ol>
If any of the preceding steps fail, the text range should be left unchanged.  If the text range cannot be moved as far as the requested number of text units, but can be moved by a smaller number of text units, the text range should be moved by the smaller number of text units and <i>pRetVal</i> should be set to the number of text units moved successfully.

For a degenerate text range, <b>ITextRangeProvider::Move</b> should simply move the text insertion point by the specified number of text units. 

When moving a text range, the provider should ignore the boundaries of any embedded objects in the text.

<b>ITextRangeProvider::Move</b> should respect both hidden and visible text. 
            

If a text-based control does not support the text unit specified by the <i>unit</i> parameter, the provider should substitute the next larger supported text unit. 
        
The size of the text units, from smallest unit to largest, is as follows.

<ul>
<li>Character
        </li>
<li>Format
        </li>
<li>Word
        </li>
<li>Line
        </li>
<li>Paragraph
        </li>
<li>Page
        </li>
<li>Document
        </li>
</ul>
<h3><a id="Range_behavior_when_unit_is_TextUnit__Format"></a><a id="range_behavior_when_unit_is_textunit__format"></a><a id="RANGE_BEHAVIOR_WHEN_UNIT_IS_TEXTUNIT__FORMAT"></a>Range behavior when <i>unit</i> is <code>TextUnit::Format</code></h3>
<code>TextUnit::Format</code> as a <i>unit</i> value positions the boundary of a text range to expand or move the range based on shared text attributes (format) of the text within the range. However, using the format text unit should not move or expand a text range across the boundary of an embedded object, such as an image or hyperlink. For more info, see <a href="/windows/desktop/WinAuto/uiauto-uiautomationtextunits">UI Automation Text Units</a> or <a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-implementingtextandtextrange">Text and TextRange Control Patterns</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>