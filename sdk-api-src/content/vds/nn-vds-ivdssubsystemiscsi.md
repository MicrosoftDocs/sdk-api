---
UID: NN:vds.IVdsSubSystemIscsi
title: IVdsSubSystemIscsi (vds.h)
author: windows-sdk-content
description: Provides methods to query and configure iSCSI targets and portals on a subsystem.
old-location: base\ivdssubsystemiscsi.htm
tech.root: VDS
ms.assetid: e92417b7-6664-4fd7-900f-aedc83291dea
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsSubSystemIscsi, IVdsSubSystemIscsi interface [VDS], IVdsSubSystemIscsi interface [VDS],described, base.ivdssubsystemiscsi, vds/IVdsSubSystemIscsi, vdshwprv/IVdsSubSystemIscsi
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
 - IVdsSubSystemIscsi
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsSubSystemIscsi interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and configure iSCSI targets and portals on a subsystem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystemIscsi</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsSubSystemIscsi</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystemIscsi</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/084a1f0e-0764-404a-bd9a-a724e4f12c5f">CreateTarget</a>
</td>
<td align="left" width="63%">
Creates an iSCSI target.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/277cc256-ac9d-4a4c-b154-ba611c08db9f">QueryPortals</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI portals of the subsystem.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86a89c23-beed-48d0-8d35-ed8dd39db3c6">QueryTargets</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI targets of the subsystem.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4a06e2b-09c9-438b-ba5b-b12bb846743b">SetIpsecGroupPresharedKey</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsSubSystemIscsi</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

