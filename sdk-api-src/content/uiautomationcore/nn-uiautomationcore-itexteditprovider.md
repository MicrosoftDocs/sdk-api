---
UID: NN:uiautomationcore.ITextEditProvider
title: ITextEditProvider (uiautomationcore.h)
author: windows-sdk-content
description: Extends the ITextProvider interface to enable Microsoft UI Automation providers to expose programmatic text-edit actions.
old-location: winauto\uiauto_itexteditprovider.htm
tech.root: WinAuto
ms.assetid: 6AA3F2A5-B34C-F7CB-13B3-6C62E2B67326
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextEditProvider, ITextEditProvider interface [Windows Accessibility], ITextEditProvider interface [Windows Accessibility],described, uiautomationcore/ITextEditProvider, winauto.uiauto_itexteditprovider
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/ITextEditProvider"
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ITextEditProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextEditProvider interface


## -description


Extends the  <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a> interface to enable Microsoft UI Automation providers to expose programmatic text-edit actions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextEditProvider</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>. <b>ITextEditProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextEditProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itexteditprovider-getactivecomposition">GetActiveComposition</a>
</td>
<td align="left" width="63%">
Returns the active composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itexteditprovider-getconversiontarget">GetConversionTarget</a>
</td>
<td align="left" width="63%">
Returns the current conversion target range.

</td>
</tr>
</table> 


## -remarks



Call  the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent">UiaRaiseTextEditTextChangedEvent</a> function to raise the UI Automation events that notify clients of changes. Use values of <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-texteditchangetype">TextEditChangeType</a> to describe the change. Follow the guidance given in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a> that describes when to raise the events and what payload the events should pass to UI Automation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent">UiaRaiseTextEditTextChangedEvent</a>
 

 

