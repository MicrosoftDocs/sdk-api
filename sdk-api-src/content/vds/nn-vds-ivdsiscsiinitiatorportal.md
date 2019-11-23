---
UID: NN:vds.IVdsIscsiInitiatorPortal
title: IVdsIscsiInitiatorPortal (vds.h)

description: Provides methods to query and interact with iSCSI initiator portals on the local system.
old-location: base\ivdsiscsiinitiatorportal.htm
tech.root: VDS
ms.assetid: ae64cc73-4f36-4846-a1c0-f329de6299ee

ms.date: 12/05/2018
ms.keywords: IVdsIscsiInitiatorPortal, IVdsIscsiInitiatorPortal interface [VDS], IVdsIscsiInitiatorPortal interface [VDS],described, base.ivdsiscsiinitiatorportal, vds/IVdsIscsiInitiatorPortal
ms.topic: interface
f1_keywords: 
 - "vds/IVdsIscsiInitiatorPortal"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsIscsiInitiatorPortal interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and interact with iSCSI initiator portals on the local system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiInitiatorPortal</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsIscsiInitiatorPortal</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatorportal-getinitiatoradapter">GetInitiatorAdapter</a>
</td>
<td align="left" width="63%">
Returns the initiator adapter to which the initiator portal belongs.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatorportal-getipsecsecurity">GetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatorportal-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of an initiator portal.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatorportal-setipsecsecurity">SetIpsecSecurity</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatorportal-setipsectunneladdress">SetIpsecTunnelAddress</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.</p> (Inherited from <b>IVdsIscsiInitiatorPortal</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

