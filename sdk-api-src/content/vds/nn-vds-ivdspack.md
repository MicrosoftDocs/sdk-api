---
UID: NN:vds.IVdsPack
title: IVdsPack (vds.h)
description: Provides methods to query and perform management operations on a pack containing disks and volumes.
helpviewer_keywords: ["IVdsPack","IVdsPack interface [VDS]","IVdsPack interface [VDS]","described","base.ivdspack","vds/IVdsPack"]
old-location: base\ivdspack.htm
tech.root: base
ms.assetid: 106989fe-d1dd-4c7f-b889-00a671c6e567
ms.date: 12/05/2018
ms.keywords: IVdsPack, IVdsPack interface [VDS], IVdsPack interface [VDS],described, base.ivdspack, vds/IVdsPack
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsPack
 - vds/IVdsPack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsPack
---

# IVdsPack interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides methods to query and 
   perform management operations on a pack containing disks and volumes.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsPack</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsPack</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsPack</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-adddisk">AddDisk</a>
</td>
<td align="left" width="63%">
Adds a disk to an online pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">CreateVolume</a>
</td>
<td align="left" width="63%">
Creates a volume within the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the property details of a pack object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-getprovider">GetProvider</a>
</td>
<td align="left" width="63%">
Returns the provider for the current pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-migratedisks">MigrateDisks</a>
</td>
<td align="left" width="63%">
Migrates a set of disks from one pack to another pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-querydisks">QueryDisks</a>
</td>
<td align="left" width="63%">
Enumerates the disks in the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-queryvolumes">QueryVolumes</a>
</td>
<td align="left" width="63%">
Enumerates the volumes in the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-recover">Recover</a>
</td>
<td align="left" width="63%">
Returns a failing or failed pack to a healthy state, if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-removemissingdisk">RemoveMissingDisk</a>
</td>
<td align="left" width="63%">
Removes a dynamic disk that is missing from the pack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-replacedisk">ReplaceDisk</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsswprovider-querypacks">IVdsSwProvider::QueryPacks</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/pack-object">Pack Object</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_pack_prop">VDS_PACK_PROP</a>

