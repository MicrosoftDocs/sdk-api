---
UID: NN:vdshwprv.IVdsIscsiPortalGroup
title: IVdsIscsiPortalGroup
author: windows-driver-content
description: Provides methods for performing query and configuration services on an iSCSI portal group.
old-location: base\ivdsiscsiportalgroup.htm
old-project: VDS
ms.assetid: 65d773bd-3828-4c9d-a841-bb85a53aeadc
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVdsIscsiPortalGroup, IVdsIscsiPortalGroup interface [VDS], IVdsIscsiPortalGroup interface [VDS],described, base.ivdsiscsiportalgroup, vds/IVdsIscsiPortalGroup, vdshwprv/IVdsIscsiPortalGroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vdshwprv.h
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
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsIscsiPortalGroup
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsIscsiPortalGroup interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for performing query and configuration services on an iSCSI portal group.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiPortalGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsIscsiPortalGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiPortalGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a2c1427-5137-47d4-a4b9-88a1bbc1e6c9">AddPortal</a>
</td>
<td align="left" width="63%">
Adds a portal to a portal group..</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/903f89b8-4712-4832-ba70-41a5362cbf28">Delete</a>
</td>
<td align="left" width="63%">
Deletes the portal group.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of a portal group.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9195e17-4e41-494d-b6ce-ceacfc16d6cb">GetTarget</a>
</td>
<td align="left" width="63%">
Returns the target to which the portal group belongs.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9d120bb-f195-413d-bc82-007523041d58">QueryAssociatedPortals</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the portals with which the portal group is associated.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/462562f5-69c2-413d-9cdf-f9e1176f5c20">RemovePortal</a>
</td>
<td align="left" width="63%">
Removes a portal from a portal group.</p> (Inherited from <b>IVdsIscsiPortalGroup</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

