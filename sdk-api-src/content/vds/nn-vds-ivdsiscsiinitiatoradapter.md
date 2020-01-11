---
UID: NN:vds.IVdsIscsiInitiatorAdapter
title: IVdsIscsiInitiatorAdapter (vds.h)
description: Provides methods to query and interact with iSCSI initiator adapters on the local system.
old-location: base\ivdsiscsiinitiatoradapter.htm
tech.root: VDS
ms.assetid: 3f911878-28c6-41db-ae9c-81e282aabf9d
ms.date: 12/05/2018
ms.keywords: IVdsIscsiInitiatorAdapter, IVdsIscsiInitiatorAdapter interface [VDS], IVdsIscsiInitiatorAdapter interface [VDS],described, base.ivdsiscsiinitiatoradapter, vds/IVdsIscsiInitiatorAdapter
f1_keywords:
- vds/IVdsIscsiInitiatorAdapter
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
- IVdsIscsiInitiatorAdapter
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsIscsiInitiatorAdapter interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and interact with iSCSI initiator adapters on the local system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsIscsiInitiatorAdapter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsIscsiInitiatorAdapter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of an initiator adapter.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-logintotarget">LoginToTarget</a>
</td>
<td align="left" width="63%">
Performs a manual login to an iSCSI target.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-logoutfromtarget">LogoutFromTarget</a>
</td>
<td align="left" width="63%">
Performs a manual logout from an iSCSI target on all iSCSI sessions to the specified target.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-queryinitiatorportals">QueryInitiatorPortals</a>
</td>
<td align="left" width="63%">
Returns an object that enumerates the iSCSI initiator portals of  the initiator adapter.</p> (Inherited from <b>IVdsIscsiInitiatorAdapter</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

