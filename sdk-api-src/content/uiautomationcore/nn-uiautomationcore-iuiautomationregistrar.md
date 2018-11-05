---
UID: NN:uiautomationcore.IUIAutomationRegistrar
title: IUIAutomationRegistrar
author: windows-sdk-content
description: Exposes methods for registering new control patterns, properties, and events.
old-location: winauto\uiauto_IUIAutomationRegistrar.htm
tech.root: WinAuto
ms.assetid: b5d979aa-7a87-4d6c-acdc-6e9eb19aac98
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IUIAutomationRegistrar, IUIAutomationRegistrar interface [Windows Accessibility], IUIAutomationRegistrar interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationRegistrar, uiauto_IUIAutomationRegistrar, uiautomationcore/IUIAutomationRegistrar, winauto.uiauto_IUIAutomationRegistrar
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
 - IUIAutomationRegistrar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationRegistrar interface


## -description


Exposes methods for registering new control patterns, properties, and events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationRegistrar</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationRegistrar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationRegistrar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17a95b6c-5dfb-45b3-92a9-0291b7d7120f">RegisterEvent</a>
</td>
<td align="left" width="63%">
Registers a third-party UI Automation event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aa61295-e035-4a51-9157-7cf9cfaee37a">RegisterPattern</a>
</td>
<td align="left" width="63%">
Registers a third-party control pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/225bbbec-5910-4711-b713-3409c9925be2">RegisterProperty</a>
</td>
<td align="left" width="63%">
Registers a third-party property.

</td>
</tr>
</table> 


## -remarks



The <b>IUIAutomationRegistrar</b> interface is exposed by the <a href="https://msdn.microsoft.com/0bb6826f-8e43-464d-9e12-97addfbb607d">CUIAutomationRegistrar</a> object. To obtain an instance of this object, call the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> function with a class ID of <b>CLSID_CUIAutomationRegistrar</b>.
	        




## -see-also




<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

