---
UID: NN:vds.IVdsVdProvider
title: IVdsVdProvider (vds.h)
description: Defines methods for creating and managing virtual disks.helpviewer_keywords: ["IVdsVdProvider","IVdsVdProvider interface","IVdsVdProvider interface","described","base.ivdsvdprovider","vds/IVdsVdProvider"]
old-location: base\ivdsvdprovider.htm
tech.root: VDS
ms.assetid: 812e8ac5-91c5-455a-94e7-2edf55d92cdc
ms.date: 12/05/2018
ms.keywords: IVdsVdProvider, IVdsVdProvider interface, IVdsVdProvider interface,described, base.ivdsvdprovider, vds/IVdsVdProvider
f1_keywords:
- vds/IVdsVdProvider
dev_langs:
- c++
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- IVdsVdProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVdProvider interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines methods for creating and managing virtual disks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVdProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVdProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVdProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvdprovider-addvdisk">AddVDisk</a>
</td>
<td align="left" width="63%">
Creates a virtual disk object  for an existing virtual disk file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvdprovider-createvdisk">CreateVDisk</a>
</td>
<td align="left" width="63%">
Creates a virtual disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvdprovider-getdiskfromvdisk">GetDiskFromVDisk</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a> interface pointer for a virtual disk given an <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvdprovider-getvdiskfromdisk">GetVDiskFromDisk</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a> interface pointer for the virtual disk given an <a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvdprovider-queryvdisks">QueryVDisks</a>
</td>
<td align="left" width="63%">
Returns a list of all virtual disks that are managed by the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>
 

 

