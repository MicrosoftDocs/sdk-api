---
UID: NN:uiautomationclient.IUIAutomationTextPattern2
title: IUIAutomationTextPattern2 (uiautomationclient.h)
description: Extends the IUIAutomationTextPattern interface.helpviewer_keywords: ["IUIAutomationTextPattern2","IUIAutomationTextPattern2 interface [Windows Accessibility]","IUIAutomationTextPattern2 interface [Windows Accessibility]","described","uiautomationclient/IUIAutomationTextPattern2","winauto.uiauto_iuiautomationtextpattern2"]
old-location: winauto\uiauto_iuiautomationtextpattern2.htm
tech.root: WinAuto
ms.assetid: E7160CDD-9A83-42F9-9F7B-8A8C13849E20
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextPattern2, IUIAutomationTextPattern2 interface [Windows Accessibility], IUIAutomationTextPattern2 interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTextPattern2, winauto.uiauto_iuiautomationtextpattern2
f1_keywords:
- uiautomationclient/IUIAutomationTextPattern2
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.dll
api_name:
- IUIAutomationTextPattern2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextPattern2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextPattern2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>. <b>IUIAutomationTextPattern2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTextPattern2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern2-getcaretrange">GetCaretRange</a>
</td>
<td align="left" width="63%">
Retrieves a zero-length text range at the location of the caret that belongs to the text-based control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern2-rangefromannotation">RangeFromAnnotation</a>
</td>
<td align="left" width="63%">
Retrieves a text range containing the text that is the target of the annotation associated with the specified annotation element.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithtextbasedcontrols">Working with Text-based Controls</a>
 

 

