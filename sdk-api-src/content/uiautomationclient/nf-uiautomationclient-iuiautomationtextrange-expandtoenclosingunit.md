---
UID: NF:uiautomationclient.IUIAutomationTextRange.ExpandToEnclosingUnit
title: IUIAutomationTextRange::ExpandToEnclosingUnit (uiautomationclient.h)
author: windows-sdk-content
description: Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is longer than the specified unit.
old-location: winauto\uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit.htm
tech.root: WinAuto
ms.assetid: 09ec62c1-f738-43af-bd6c-b45fdfb32236
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExpandToEnclosingUnit, ExpandToEnclosingUnit method [Windows Accessibility], ExpandToEnclosingUnit method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],ExpandToEnclosingUnit method, IUIAutomationTextRange.ExpandToEnclosingUnit, IUIAutomationTextRange::ExpandToEnclosingUnit, uiauto.uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit, uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit, uiautomationclient/IUIAutomationTextRange::ExpandToEnclosingUnit, winauto.uiauto_IUIAutomationTextRange_ExpandToEnclosingUnit
ms.topic: method
f1_keywords: ["uiautomationclient/IUIAutomationTextRange.ExpandToEnclosingUnit"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange.ExpandToEnclosingUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextRange::ExpandToEnclosingUnit


## -description


Normalizes the text range by the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is 
		  longer than the specified unit.


## -parameters






#### - textUnit [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

The text unit, such as line or paragraph.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Client applications such as screen readers use this method  to retrieve  the full word, sentence, or paragraph that exists at the insertion point or caret position.

Despite its name, the <b>ExpandToEnclosingUnit</b> method does not necessarily expand a text range. Instead, it "normalizes" a text range by moving the endpoints so that the range encompasses the specified text unit. The range is expanded if it is smaller than the specified unit, or shortened if it is longer than the specified unit. If the range is already an exact quantity of the specified units, it remains unchanged. The following diagram shows how <b>ExpandToEnclosingUnit</b> normalizes a text range by moving the endpoints of the range. 
            

<img alt="Diagram showing endpoints before and after ExpandToEnclosingUnit" src="./images/expand-to-enclosing-unit.jpg"/>
<b>ExpandToEnclosingUnit</b> defaults to the next largest text unit 
        supported if the specified text unit is not supported by the control. 
        
        The order, from smallest unit to largest, is as follows:
        

<ul>
<li><i>Character</i></li>
<li><i>Format</i></li>
<li><i>Word</i></li>
<li><i>Line</i></li>
<li><i>Paragraph</i></li>
<li><i>Page</i></li>
<li><i>Document</i></li>
</ul>
<b>ExpandToEnclosingUnit</b> respects both visible and hidden text. 
        

<h3><a id="Range_behavior_when_unit_is_TextUnit__Format"></a><a id="range_behavior_when_unit_is_textunit__format"></a><a id="RANGE_BEHAVIOR_WHEN_UNIT_IS_TEXTUNIT__FORMAT"></a>Range behavior when <i>unit</i> is <code>TextUnit::Format</code></h3>
<code>TextUnit::Format</code> as a <i>unit</i> value positions the boundary of a text range to expand or move the range based on shared text attributes (format) of the text within the range. However, using the format text unit will not move or expand a text range across the boundary of an embedded object, such as an image or hyperlink. For more info, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-uiautomationtextunits">UI Automation Text Units</a> or <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
 

 

