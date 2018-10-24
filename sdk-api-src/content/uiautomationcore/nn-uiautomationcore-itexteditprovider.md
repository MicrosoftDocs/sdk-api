---
UID: NN:uiautomationcore.ITextEditProvider
title: ITextEditProvider
author: windows-sdk-content
description: Extends the ITextProvider interface to enable Microsoft UI Automation providers to expose programmatic text-edit actions.
old-location: winauto\uiauto_itexteditprovider.htm
tech.root: WinAuto
ms.assetid: 6AA3F2A5-B34C-F7CB-13B3-6C62E2B67326
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: ITextEditProvider, ITextEditProvider interface [Windows Accessibility], ITextEditProvider interface [Windows Accessibility],described, uiautomationcore/ITextEditProvider, winauto.uiauto_itexteditprovider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# ITextEditProvider interface


## -description


Extends the  <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a> interface to enable Microsoft UI Automation providers to expose programmatic text-edit actions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextEditProvider</b> interface inherits from <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>. <b>ITextEditProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/E0A4E340-8F23-8EE0-31E4-90DB8D8E68FF">GetActiveComposition</a>
</td>
<td align="left" width="63%">
Returns the active composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C05DC0F6-FB24-2D06-C2D8-43ADF2C110F9">GetConversionTarget</a>
</td>
<td align="left" width="63%">
Returns the current conversion target range.

</td>
</tr>
</table> 


## -remarks



Call  the <a href="https://msdn.microsoft.com/19E7C2C1-D0D5-672F-FC6F-8E1B8CC19819">UiaRaiseTextEditTextChangedEvent</a> function to raise the UI Automation events that notify clients of changes. Use values of <a href="https://msdn.microsoft.com/212FD71E-BB79-F4A5-061E-F77FF7876998">TextEditChangeType</a> to describe the change. Follow the guidance given in <a href="https://msdn.microsoft.com/AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9">TextEdit Control Pattern</a> that describes when to raise the events and what payload the events should pass to UI Automation.




## -see-also




<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/AA9E04AC-1AC0-6434-ADEF-9FF82ADA7CD9">TextEdit Control Pattern</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>



<a href="https://msdn.microsoft.com/19E7C2C1-D0D5-672F-FC6F-8E1B8CC19819">UiaRaiseTextEditTextChangedEvent</a>
 

 

