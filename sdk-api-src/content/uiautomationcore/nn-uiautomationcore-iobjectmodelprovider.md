---
UID: NN:uiautomationcore.IObjectModelProvider
title: IObjectModelProvider
author: windows-sdk-content
description: Provides access to the underlying object model implemented by a control or application.
old-location: winauto\uiauto_IObjectModelProvider.htm
tech.root: WinAuto
ms.assetid: E374F95B-9F0A-41D6-A916-F5CD5F5E442D
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IObjectModelProvider, IObjectModelProvider interface [Windows Accessibility], IObjectModelProvider interface [Windows Accessibility],described, uiautomationcore/IObjectModelProvider, winauto.uiauto_IObjectModelProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IObjectModelProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectModelProvider interface


## -description


Provides access to the underlying object model implemented by a control or application.   Assistive technology applications can use the object model to directly access the content of the control or application. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectModelProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectModelProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectModelProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/305758A1-D584-45A3-B118-B46B3731820D">GetUnderlyingObjectModel</a>
</td>
<td align="left" width="63%">
Retrieves an interface used to access the underlying object model of the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/08d0226d-845c-4564-a059-539b62fc7909">Control Pattern Interfaces for Providers</a>
 

 

