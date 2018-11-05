---
UID: NN:objidl.IGlobalInterfaceTable
title: IGlobalInterfaceTable
author: windows-sdk-content
description: Enables any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.
old-location: com\iglobalinterfacetable.htm
tech.root: com
ms.assetid: 0c1feee7-e33b-4b5d-8e35-4de6895e3947
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IGlobalInterfaceTable, IGlobalInterfaceTable interface [COM], IGlobalInterfaceTable interface [COM],described, _com_iglobalinterfacetable, com.iglobalinterfacetable, objidl/IGlobalInterfaceTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IGlobalInterfaceTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGlobalInterfaceTable interface


## -description


Enables any apartment in a process to get access to an interface implemented on an object in any other apartment in the process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGlobalInterfaceTable</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IGlobalInterfaceTable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGlobalInterfaceTable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b37184d-c4e8-47b2-8f3f-008d3ea00759">GetInterfaceFromGlobal</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an interface on an object that is usable by the calling apartment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5282b0b8-4eab-4114-8061-6d74db3756b7">RegisterInterfaceInGlobal</a>
</td>
<td align="left" width="63%">
Registers the specified interface on an object residing in one apartment of a process as a global interface, enabling other apartments access to that interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/202bf33a-5827-4cbf-b977-86167a9c633f">RevokeInterfaceFromGlobal</a>
</td>
<td align="left" width="63%">
Revokes the registration of an interface in the global interface table.

</td>
</tr>
</table> 


## -remarks



The <b>IGlobalInterfaceTable</b> interface is an efficient way for a process to store an interface pointer in a memory location that can be accessed from multiple apartments within the process, such as processwide variables and agile (free-threaded marshaled) objects containing interface pointers to other objects. 



An agile object is unaware of the underlying COM infrastructure in which it runsâ€”in other words, what apartment, context, and thread it is executing on. The object may be holding on to interfaces that are specific to an apartment or context. For this reason, calling these interfaces from wherever the agile component is executing may not always work properly. The global interface table avoids this problem by guaranteeing that a valid proxy (or direct pointer) to the object is used, based on where the agile object is executing.

The global interface table is not portable across process or machine boundaries, so it cannot be used in place of the normal parameter-passing mechanism. 





