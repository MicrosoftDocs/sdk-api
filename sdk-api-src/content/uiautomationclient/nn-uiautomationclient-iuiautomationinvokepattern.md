---
UID: NN:uiautomationclient.IUIAutomationInvokePattern
title: IUIAutomationInvokePattern
author: windows-sdk-content
description: Exposes a method that enables a client application to invoke the action of a control (typically a button).
old-location: winauto\uiauto_IUIAutomationInvokePattern.htm
tech.root: WinAuto
ms.assetid: 08031f22-9b36-4d85-9e15-2139551b893b
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IUIAutomationInvokePattern, IUIAutomationInvokePattern interface [Windows Accessibility], IUIAutomationInvokePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationInvokePattern, uiauto_IUIAutomationInvokePattern, uiautomationclient/IUIAutomationInvokePattern, winauto.uiauto_IUIAutomationInvokePattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IUIAutomationInvokePattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationInvokePattern interface


## -description


Exposes a method that enables a client application to invoke the action of a control (typically a button).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationInvokePattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationInvokePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationInvokePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd04426c-edc5-4ee9-95ac-22f32fb14daa">Invoke</a>
</td>
<td align="left" width="63%">
Invokes the action of a control, such as a button click.

</td>
</tr>
</table> 


## -remarks



A control should support this interface if it initiates or performs a single, unambiguous action and does not maintain state when activated.        
            




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

