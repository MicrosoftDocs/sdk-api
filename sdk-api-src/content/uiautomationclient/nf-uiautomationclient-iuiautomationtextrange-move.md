---
UID: NF:uiautomationclient.IUIAutomationTextRange.Move
title: IUIAutomationTextRange::Move
author: windows-sdk-content
description: Moves the text range forward or backward by the specified number of text units .
old-location: winauto\uiauto_IUIAutomationTextRange_Move.htm
old-project: WinAuto
ms.assetid: b59ffdb5-6c05-4139-84ae-10ca5c543c3c
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],Move method, IUIAutomationTextRange.Move, IUIAutomationTextRange::Move, Move, Move method [Windows Accessibility], Move method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_Move, uiauto_IUIAutomationTextRange_Move, uiautomationclient/IUIAutomationTextRange::Move, winauto.uiauto_IUIAutomationTextRange_Move
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange.Move
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRange::Move


## -description


Moves the text range forward or backward by the specified number of text units .


## -parameters




### -param unit [in]

Type: <b><a href="https://msdn.microsoft.com/518318fc-d60f-41b7-a6da-1f2bf5c2e494">TextUnit</a></b>

A value specifying the type of text units, such as character, word, paragraph, and so on.


### -param count [in]

Type: <b>int</b>

The number of text units to move. A positive value moves the text range forward. A negative value moves the text range backward. Zero has no effect.


### -param moved [out, retval]

Type: <b>int*</b>

Receives the number of text units actually moved. This can be less than the number requested if either of the new text range endpoints is greater than or less than the endpoints retrieved by the <a href="https://msdn.microsoft.com/38892548-7c1f-4bac-8eac-29d7b4d190d3">IUIAutomationTextPattern::DocumentRange</a> method. This value can be negative if navigation is happening in the backward direction.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IUIAutomationTextRange::Move</b> moves the text range to span a different part of the text; it does not alter the text in any way.

            
            


			  For a non-degenerate (non-empty) text range, <b>IUIAutomationTextRange::Move</b> normalizes and moves the range by performing the following steps.
            

<ol>
<li>The text range is collapsed to a degenerate (empty) range at the starting endpoint.</li>
<li>If necessary, the resulting text range is moved backward in the document to the beginning of the requested text unit boundary.</li>
<li>The text range is moved forward or backward in the document by the requested number of text unit boundaries.</li>
<li>The text range is expanded from the degenerate state by moving the ending endpoint forward by one requested text unit boundary. </li>
</ol>
If any of the preceding steps fail, the text range is left unchanged.  If the text range cannot be moved as far as the requested number of text units, but can be moved by a smaller number of text units, the text range is moved by the smaller number of text units and <i>moved</i> is set to the number of text units moved.


            For a degenerate text range, <b>IUIAutomationTextRange::Move</b> simply moves the 
            text insertion point by the specified number of text units. 

When moving a text range, <b>IUIAutomationTextRange::Move</b> ignores the boundaries of any embedded objects in the text.

<b>IUIAutomationTextRange::Move</b> respects both hidden and visible text. 
            

If a text-based control does not support the text unit specified by the <i>unit</i> parameter, <b>IUIAutomationTextRange::Move</b> substitutes the next larger supported text unit. 
        
        The size of the text units, from smallest unit to largest, is as follows.

<ul>
<li>
        Character
        </li>
<li>
        Format
        </li>
<li>
        Word
        </li>
<li>
        Line
        </li>
<li>
        Paragraph
        </li>
<li>
        Page
        </li>
<li>
        Document
        </li>
</ul>
<h3><a id="Range_behavior_when_unit_is_TextUnit__Format"></a><a id="range_behavior_when_unit_is_textunit__format"></a><a id="RANGE_BEHAVIOR_WHEN_UNIT_IS_TEXTUNIT__FORMAT"></a>Range behavior when <i>unit</i> is <code>TextUnit::Format</code></h3>
<code>TextUnit::Format</code> as a <i>unit</i> value positions the boundary of a text range to expand or move the range based on shared text attributes (format) of the text within the range. However, using the format text unit will not move or expand a text range across the boundary of an embedded object, such as an image or hyperlink. For more info, see <a href="https://msdn.microsoft.com/3ec43a81-c4f1-4c73-865f-a60c751fc3fb">UI Automation Text Units</a> or <a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

