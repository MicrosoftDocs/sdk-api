---
UID: NF:oleidl.IOleClientSite.GetContainer
title: IOleClientSite::GetContainer
author: windows-driver-content
description: Retrieves a pointer to the object's container.
old-location: com\ioleclientsite_getcontainer.htm
old-project: com
ms.assetid: 8f0caf07-f059-4e0c-9c28-c7ad0cc149e3
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetContainer, GetContainer method [COM], GetContainer method [COM],IOleClientSite interface, IOleClientSite interface [COM],GetContainer method, IOleClientSite.GetContainer, IOleClientSite::GetContainer, _ole_ioleclientsite_getcontainer, com.ioleclientsite_getcontainer, oleidl/IOleClientSite::GetContainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleClientSite.GetContainer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleClientSite::GetContainer


## -description


Retrieves a pointer to the object's container.


## -parameters




### -param ppContainer [out]

Address of <a href="https://msdn.microsoft.com/98549309-8ac8-4391-92ab-8a62269ff579">IOleContainer</a> pointer variable that receives the interface pointer to the container object. If an error occurs, the implementation must set <i>ppContainer</i> to <b>NULL</b>.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The client site is in an OLE 1 container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The container does not implement the <a href="https://msdn.microsoft.com/98549309-8ac8-4391-92ab-8a62269ff579">IOleContainer</a> interface.

</td>
</tr>
</table>
 




## -remarks



If a container supports links to its embedded objects, implementing <b>GetContainer</b> enables link clients to enumerate the container's objects and recursively traverse a containment hierarchy. This method is optional but recommended for all containers that expect to support links to their embedded objects.

Link clients can traverse a hierarchy of compound-document objects by recursively calling <b>GetContainer</b> to get a pointer to the link source's container; followed by <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to get a pointer to the container's <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface and, finally, <a href="https://msdn.microsoft.com/bf26b989-445c-48d3-b279-29e4cef0ad97">IOleObject::GetClientSite</a> to get the container's client site in its container.

Simple containers that do not support links to their embedded objects probably do not need to implement this method. Instead, they can return E_NOINTERFACE and set <i>ppContainer</i> to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/dafee149-926a-4d08-a43d-5847682db645">IOleClientSite</a>
 

 

