---
UID: NN:uiautomationcore.IItemContainerProvider
title: IItemContainerProvider
author: windows-sdk-content
description: Provides access to controls that act as containers of other controls, such as a virtual list-view.
old-location: winauto\uiauto_IItemContainerProvider.htm
tech.root: WinAuto
ms.assetid: 403436f5-7540-455b-965e-e2e3b64ef7e0
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IItemContainerProvider, IItemContainerProvider interface [Windows Accessibility], IItemContainerProvider interface [Windows Accessibility],described, uiauto.uiauto_IItemContainerProvider, uiauto_IItemContainerProvider, uiautomationcore/IItemContainerProvider, winauto.uiauto_IItemContainerProvider
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
 - IItemContainerProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IItemContainerProvider interface


## -description


Provides access to controls that act as containers of other controls, such as a virtual list-view.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IItemContainerProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IItemContainerProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IItemContainerProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2873bbb-5bb4-4eaa-b0bd-60061fc06f53">FindItemByProperty</a>
</td>
<td align="left" width="63%">
Retrieves an element within a containing element, based on a specified property value.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/6f3dd94e-3563-4a13-9db9-5928a02bab77">ItemContainer</a> control pattern allows a container object to efficiently lookup an item by a 
		specified automation element property, such as Name, AutomationId, or IsSelected state. While this control 
		pattern is introduced with a view to being used by virtualized containers, it can be implemented by any container 
		that provides name lookup, independently of whether that container uses virtualization.




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

