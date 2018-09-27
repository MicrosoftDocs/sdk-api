---
UID: NN:shobjidl_core.IHandlerInfo
title: IHandlerInfo
author: windows-sdk-content
description: Supplies methods that provide information about the handler to methods of the IHandlerActivationHost interface.
old-location: shell\IHandlerInfo.htm
tech.root: shell
ms.assetid: f0b8da9f-75ee-418d-8df6-fa0d7c600e62
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IHandlerInfo, IHandlerInfo interface [Windows Shell], IHandlerInfo interface [Windows Shell],described, shell.IHandlerInfo, shobjidl_core/IHandlerInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IHandlerInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHandlerInfo interface


## -description


Supplies methods that provide information about the handler to methods of the <a href="https://msdn.microsoft.com/4c60a3f8-48ec-4686-9e27-692f88cd1c55">IHandlerActivationHost</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHandlerInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHandlerInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHandlerInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19b3b042-7c2d-4402-913e-daa5c8bba595">GetApplicationDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the application that implemented the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be886508-16a5-4a77-9fa4-b6a8d028c9e9">GetApplicationIconReference</a>
</td>
<td align="left" width="63%">
Retrieves the icon of the application that implemented the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5e22afa-69eb-4cf5-98b0-f46e25fb136e">GetApplicationPublisher</a>
</td>
<td align="left" width="63%">
Retrieves the name of the publisher of the application that implemented the handler.

</td>
</tr>
</table> 

