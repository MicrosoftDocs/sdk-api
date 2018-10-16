---
UID: NN:uiautomationcore.IUIAutomationPatternHandler
title: IUIAutomationPatternHandler
author: windows-sdk-content
description: Returns a client API wrapper object and to unmarshal property and method requests to an actual provider instance.
old-location: winauto\uiauto_IUIAutomationPatternHandler.htm
tech.root: WinAuto
ms.assetid: 6d0edd8e-3fd4-47d6-ab53-582eb81f38bd
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IUIAutomationPatternHandler, IUIAutomationPatternHandler interface [Windows Accessibility], IUIAutomationPatternHandler interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationPatternHandler, uiauto_IUIAutomationPatternHandler, uiautomationcore/IUIAutomationPatternHandler, winauto.uiauto_IUIAutomationPatternHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IUIAutomationPatternHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationPatternHandler interface


## -description


Returns a client API wrapper object and to unmarshal property and method requests to an actual provider instance. The PatternHandler object is stateless, so this can be implemented by a singleton.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationPatternHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationPatternHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationPatternHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03530381-52f8-4d9b-a54c-faebf7cd4a06">CreateClientWrapper</a>
</td>
<td align="left" width="63%">
Creates an object that enables a client application to interact with a custom <i>control pattern</i>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c94d650e-74a8-4d4f-92bf-5402576f8773">Dispatch</a>
</td>
<td align="left" width="63%">
Dispatches a method or property getter to a custom <i>control pattern</i> provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

