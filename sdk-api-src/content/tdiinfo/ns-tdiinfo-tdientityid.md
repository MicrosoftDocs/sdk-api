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

# TDIEntityID structure


## -description


<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Contains a part of the <a href="https://msdn.microsoft.com/79d34f1c-2ea7-4867-9fb2-80401b0859bf">TDIObjectID</a> structure to represent information about TDI drivers retrieved using the <a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a> control code.


## -struct-fields




### -field tei_entity

The type of entity being addressed. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GENERIC_ENTITY"></a><a id="generic_entity"></a><dl>
<dt><b>GENERIC_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Used when requesting a list of all entities.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_ENTITY"></a><a id="at_entity"></a><dl>
<dt><b>AT_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies an address-translation (AT) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CL_NL_ENTITY"></a><a id="cl_nl_entity"></a><dl>
<dt><b>CL_NL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connectionless (CL) network-layer (NL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CO_NL_ENTITY"></a><a id="co_nl_entity"></a><dl>
<dt><b>CO_NL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connected, directed-packet (CO) network-layer (NL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CL_TL_ENTITY"></a><a id="cl_tl_entity"></a><dl>
<dt><b>CL_TL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connectionless (CL) transport-layer (TL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CO_TL_ENTITY"></a><a id="co_tl_entity"></a><dl>
<dt><b>CO_TL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connected, directed-packet (CO) transport-layer (TL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="ER_ENTITY"></a><a id="er_entity"></a><dl>
<dt><b>ER_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies an Echo-Request/Echo-Reply (ER) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_ENTITY"></a><a id="if_entity"></a><dl>
<dt><b>IF_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies an interface entity.

</td>
</tr>
</table>
 


### -field tei_instance

An opaque value that can uniquely identify an entity, if a specific one is being addressed.


## -see-also




<a href="https://msdn.microsoft.com/b992b585-e1c8-4262-a6e0-ad8b5047620f">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/566bf187-73d0-4d61-be8e-306dc482a005">Management Information Base
			 Reference</a>



<a href="https://msdn.microsoft.com/79d34f1c-2ea7-4867-9fb2-80401b0859bf">TDIObjectID</a>
 

 

