---
UID: NN:vds.IVdsIscsiInitiatorAdapter
title: IVdsIscsiInitiatorAdapter
author: windows-sdk-content
description: Provides methods to query and interact with iSCSI initiator adapters on the local system.
old-location: base\ivdsiscsiinitiatoradapter.htm
tech.root: VDS
ms.assetid: 3f911878-28c6-41db-ae9c-81e282aabf9d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVdsIscsiInitiatorAdapter, IVdsIscsiInitiatorAdapter interface [VDS], IVdsIscsiInitiatorAdapter interface [VDS],described, base.ivdsiscsiinitiatoradapter, vds/IVdsIscsiInitiatorAdapter
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
 - IVdsIscsiInitiatorAdapter
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiInitiatorAdapter interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and interact with iSCSI initiator adapters on the local system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiInitiatorAdapter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsIscsiInitiatorAdapter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiInitiatorAdapter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9442e182-bc2e-47dd-9ddc-aa1a618a5563">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of an initiator adapter.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74d6ddd0-1b78-446a-9bce-6816eb34a2b9">LoginToTarget</a>
</td>
<td align="left" width="63%">
Performs a manual login to an iSCSI target.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2f7598c-c532-4b68-b581-40b3f5eed1bf">LogoutFromTarget</a>
</td>
<td align="left" width="63%">
Performs a manual logout from an iSCSI target on all iSCSI sessions to the specified target.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3c893c0-167f-46f5-92f8-aa61f5e16542">QueryInitiatorPortals</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI initiator portals of  the initiator adapter.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

