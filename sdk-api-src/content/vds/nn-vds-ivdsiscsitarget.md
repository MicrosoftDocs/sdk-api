---
UID: NN:vds.IVdsIscsiTarget
title: IVdsIscsiTarget (vds.h)
author: windows-sdk-content
description: Provides methods for performing query and configuration operations on an iSCSI target.
old-location: base\ivdsiscsitarget.htm
tech.root: VDS
ms.assetid: 0db442c4-6cc1-43b2-8ac8-8b17cadb1101
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsIscsiTarget, IVdsIscsiTarget interface [VDS], IVdsIscsiTarget interface [VDS],described, base.ivdsiscsitarget, vds/IVdsIscsiTarget, vdshwprv/IVdsIscsiTarget
ms.topic: interface
f1_keywords: 
 - "vds/IVdsIscsiTarget"
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
 - IVdsIscsiTarget
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsIscsiTarget interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides 
   methods for performing query and configuration operations on an iSCSI target.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiTarget</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsIscsiTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsIscsiTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-createportalgroup">CreatePortalGroup</a>
</td>
<td align="left" width="63%">
Creates a portal group.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the target and all of its portal groups if no LUNs are associated with the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-getconnectedinitiators">GetConnectedInitiators</a>
</td>
<td align="left" width="63%">
Returns the list of iSCSI names of the initiators currently logged into the 
   target.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of an iSCSI target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-getsubsystem">GetSubSystem</a>
</td>
<td align="left" width="63%">
Returns the subsystem to which the target belongs.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-queryassociatedluns">QueryAssociatedLuns</a>
</td>
<td align="left" width="63%">
Returns an enumeration of the LUNs associated with the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-queryportalgroups">QueryPortalGroups</a>
</td>
<td align="left" width="63%">
Returns an  enumeration of the iSCSI portal groups within the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-rememberinitiatorsharedsecret">RememberInitiatorSharedSecret</a>
</td>
<td align="left" width="63%">
Communicates the initiator CHAP secret used for mutual CHAP authentication when the initiator 
     authenticates the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-setfriendlyname">SetFriendlyName</a>
</td>
<td align="left" width="63%">
Sets the friendly name of the target.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-setsharedsecret">SetSharedSecret</a>
</td>
<td align="left" width="63%">
Sets the target CHAP secret used for CHAP authentication when the target authenticates the 
     initiator.</p> (Inherited from <b>IVdsIscsiTarget</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

