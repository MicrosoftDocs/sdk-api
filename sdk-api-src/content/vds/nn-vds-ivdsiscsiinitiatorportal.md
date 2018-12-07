---
UID: NN:vds.IVdsIscsiInitiatorPortal
title: IVdsIscsiInitiatorPortal
author: windows-sdk-content
description: Provides methods to query and interact with iSCSI initiator portals on the local system.
old-location: base\ivdsiscsiinitiatorportal.htm
tech.root: vds
ms.assetid: ae64cc73-4f36-4846-a1c0-f329de6299ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsIscsiInitiatorPortal, IVdsIscsiInitiatorPortal interface [VDS], IVdsIscsiInitiatorPortal interface [VDS],described, base.ivdsiscsiinitiatorportal, vds/IVdsIscsiInitiatorPortal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsIscsiInitiatorPortal
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiInitiatorPortal interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and interact with iSCSI initiator portals on the local system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiInitiatorPortal</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsIscsiInitiatorPortal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiInitiatorPortal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcdd2083-36e0-4924-9af0-87a9fe4711e0">GetInitiatorAdapter</a>
</td>
<td align="left" width="63%">
Returns the initiator adapter to which the initiator portal belongs.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/755ff0fb-c61f-4427-b7dc-a91dd203fb64">GetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bf00853-ca26-40b4-a09a-dcb5e7e08f49">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of an initiator portal.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67dba1b5-268a-4598-8d48-a8f42e80eb9d">SetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40fd4eb5-afe1-4947-81b2-df44c273efe1">SetIpsecTunnelAddress</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

