---
UID: NN:vdshwprv.IVdsIscsiPortal
title: IVdsIscsiPortal
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on an iSCSI portal.
old-location: base\ivdsiscsiportal.htm
old-project: vds
ms.assetid: 1f3131a6-01ab-41e5-9e2f-6ffcdcd0e3a6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsIscsiPortal, IVdsIscsiPortal interface [VDS], IVdsIscsiPortal interface [VDS],described, base.ivdsiscsiportal, vds/IVdsIscsiPortal, vdshwprv/IVdsIscsiPortal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vdshwprv.h
req.include-header: 
req.redist: VDS 1.1
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsIscsiPortal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsIscsiPortal interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides 
   methods for performing query and configuration operations on an iSCSI portal.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiPortal</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsIscsiPortal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiPortal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c815856f-94a2-4748-b9ac-54a2ef69c97e">GetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a17597d5-2525-4a0c-acb3-dc69a6ef04ce">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of a portal.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e222cdc-6399-4e28-b59b-ba912e32eb9d">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the portal belongs.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b8dbfc8-9112-4ca9-9976-ac3bf859588d">QueryAssociatedPortalGroups</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the portal groups with which the portal is associated.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73209e3c-f1c9-411e-b272-4d4a2b168824">SetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/200ac111-7029-4bfa-a08b-b4bce3c86bb7">SetIpsecTunnelAddress</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c63fa36-bccb-4731-999a-c6f8b565b38f">SetStatus</a>
</td>
<td align="left" width="63%">
Sets the status of a portal to the specified value.</p> (Inherited from <b>IVdsIscsiPortal</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

