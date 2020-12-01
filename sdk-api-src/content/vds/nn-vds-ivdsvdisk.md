---
UID: NN:vds.IVdsVDisk
title: IVdsVDisk (vds.h)
description: Defines methods for managing a virtual disk.
helpviewer_keywords: ["IVdsVDisk","IVdsVDisk interface","IVdsVDisk interface","described","base.ivdsvdisk","vds/IVdsVDisk"]
old-location: base\ivdsvdisk.htm
tech.root: base
ms.assetid: 2b4f81f9-81ec-4288-a26c-8ed4d378358a
ms.date: 12/05/2018
ms.keywords: IVdsVDisk, IVdsVDisk interface, IVdsVDisk interface,described, base.ivdsvdisk, vds/IVdsVDisk
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsVDisk
 - vds/IVdsVDisk
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
 - IVdsVDisk
---

# IVdsVDisk interface


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines methods for managing a virtual disk.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVDisk</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVdsVDisk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVDisk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vds/nf-vds-ivdsvdisk-getdevicename">GetDeviceName</a>
</td>
<td align="left" width="63%">
Returns the device name for the volume where the virtual disk resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vds/nf-vds-ivdsvdisk-gethostvolume">GetHostVolume</a>
</td>
<td align="left" width="63%">
Returns an interface pointer to the volume object for the volume where the virtual disk resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vds/nf-vds-ivdsvdisk-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Returns disk property information for the volume where the virtual disk resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vds/nf-vds-ivdsvdisk-open">Open</a>
</td>
<td align="left" width="63%">
Opens a handle to the specified virtual disk file and returns an <a href="/windows/desktop/api/vds/nn-vds-ivdsopenvdisk">IVdsOpenVDisk</a> interface pointer to the object that represents the opened handle.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvdprovider">IVdsVdProvider</a>



<a href="/windows/desktop/VDS/vds-interfaces">VDS Interfaces</a>