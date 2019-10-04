---
UID: NN:uiautomationclient.IUIAutomationTextRange3
title: IUIAutomationTextRange3 (uiautomationclient.h)
author: windows-sdk-content
description: Extends the IUIAutomationTextRange2 interface to support faster access to the underlying rich text data on a text range.
old-location: winauto\uiauto_IUIAutomationTextRange3.htm
tech.root: WinAuto
ms.assetid: 3491996E-89EF-496D-94B6-FF8D121D3828
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange3, IUIAutomationTextRange3 interface [Windows Accessibility], IUIAutomationTextRange3 interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTextRange3, winauto.uiauto_IUIAutomationTextRange3
ms.topic: interface
f1_keywords: 
 - "uiautomationclient/IUIAutomationTextRange3"
dev_langs:
 - c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IUIAutomationTextRange3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextRange3 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange2">IUIAutomationTextRange2</a> interface to support faster access to the underlying rich text data on a text range.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextRange3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange2">IUIAutomationTextRange2</a>. <b>IUIAutomationTextRange3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTextRange3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange3-getattributevalues">GetAttributeValues</a>
</td>
<td align="left" width="63%">
Returns all of the requested text attribute values for a text range in a single cross-process call.  This is equivalent to calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue">GetAttributeValue</a>, except it can retrieve multiple values instead of just one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange3-getchildrenbuildcache">GetChildrenBuildCache</a>
</td>
<td align="left" width="63%">
Returns the children and supplied properties and patterns for elements in a text range in a single cross-process call.  This is equivalent to calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getchildren">GetChildren</a>, but adds the standard build cache pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange3-getenclosingelementbuildcache">GetEnclosingElementBuildCache</a>
</td>
<td align="left" width="63%">
Gets the enclosing element and supplied properties and patterns for an element in a text range in a single cross-process call.  This is equivalent to calling <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement">GetEnclosingElement</a>, but adds the standard build cache pattern.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange2">IUIAutomationTextRange2</a>
 

 

