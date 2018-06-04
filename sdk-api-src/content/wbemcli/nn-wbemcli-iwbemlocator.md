---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWbemLocator interface


## -description


Use the 
<b>IWbemLocator</b> interface to obtain the initial namespace pointer to the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface for WMI on a specific host computer. You can access Windows Management itself using the 
<b>IWbemServices</b> pointer, which is returned by the 
<a href="https://msdn.microsoft.com/92222e08-8622-46c3-9465-cd12260a2ca0">IWbemLocator::ConnectServer</a> method.

A client or provider that requires Windows Management services first obtains a pointer to the locator using <a href="_com_cocreateinstance">CoCreateInstance</a> or <a href="_com_cocreateinstanceex">CoCreateInstanceEx</a>, as specified in the COM documentation in the Microsoft Windows Software Development Kit (SDK). The 
<b>IWbemLocator</b> object is always an in-process COM server. The interface pointer to the desired namespace on the desired target computer is then obtained through the 
<a href="https://msdn.microsoft.com/92222e08-8622-46c3-9465-cd12260a2ca0">IWbemLocator::ConnectServer</a> method, which is the only method on this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemLocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92222e08-8622-46c3-9465-cd12260a2ca0">ConnectServer</a>
</td>
<td align="left" width="63%">
Connects to Windows Management on the specified computer.

</td>
</tr>
</table> 

