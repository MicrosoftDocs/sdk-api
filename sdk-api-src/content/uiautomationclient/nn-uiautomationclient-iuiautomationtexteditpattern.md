---
UID: NN:uiautomationclient.IUIAutomationTextEditPattern
title: IUIAutomationTextEditPattern (uiautomationclient.h)
author: windows-sdk-content
description: Provides access to a control that modifies text, for example a control that performs auto-correction or enables input composition through an Input Method Editor (IME).
old-location: winauto\uiauto_IUIAutomationTextEditPattern.htm
tech.root: WinAuto
ms.assetid: 798FABE5-D6C8-58E3-B3F6-93654C0F4CAB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextEditPattern, IUIAutomationTextEditPattern interface [Windows Accessibility], IUIAutomationTextEditPattern interface [Windows Accessibility],described, uiautomationclient/IUIAutomationTextEditPattern, winauto.uiauto_IUIAutomationTextEditPattern
ms.topic: interface
f1_keywords: 
 - "uiautomationclient/IUIAutomationTextEditPattern"
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IUIAutomationTextEditPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextEditPattern interface


## -description


Provides access to a control that modifies text, for example a control that performs auto-correction or enables input composition through an Input Method Editor (IME).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTextEditPattern</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>. <b>IUIAutomationTextEditPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationTextEditPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtexteditpattern-getactivecomposition">GetActiveComposition</a>
</td>
<td align="left" width="63%">
Returns the active composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtexteditpattern-getconversiontarget">GetConversionTarget</a>
</td>
<td align="left" width="63%">
Returns the current conversion target range.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>
 

 

