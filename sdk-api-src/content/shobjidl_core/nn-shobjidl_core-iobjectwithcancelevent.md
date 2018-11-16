---
UID: NN:shobjidl_core.IObjectWithCancelEvent
title: IObjectWithCancelEvent
author: windows-sdk-content
description: Not supported.Supplies a caller with an event that will be signaled by the called object to denote cancellation of a task.
old-location: shell\IObjectWithCancelEvent.htm
tech.root: shell
ms.assetid: 3bac219d-d9fd-4259-8f34-032554291327
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IObjectWithCancelEvent, IObjectWithCancelEvent interface [Windows Shell], IObjectWithCancelEvent interface [Windows Shell],described, _shell_IObjectWithCancelEvent, shell.IObjectWithCancelEvent, shobjidl_core/IObjectWithCancelEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IObjectWithCancelEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithCancelEvent interface


## -description


Not supported.

Supplies a caller with an event that will be signaled by the called object to denote cancellation of a task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithCancelEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectWithCancelEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithCancelEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aef54b0-a7aa-4ff9-b50f-f84131614853">GetCancelEvent</a>
</td>
<td align="left" width="63%">
Retrieves an event that will be sent when an operation is cancelled.

</td>
</tr>
</table> 

