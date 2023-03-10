---
UID: NF:vds.IVdsDisk.QueryExtents
title: IVdsDisk::QueryExtents (vds.h)
description: Returns the details of all the extents on a disk.
helpviewer_keywords: ["IVdsDisk interface [VDS]","QueryExtents method","IVdsDisk.QueryExtents","IVdsDisk::QueryExtents","QueryExtents","QueryExtents method [VDS]","QueryExtents method [VDS]","IVdsDisk interface","base.ivdsdisk_queryextents","vds/IVdsDisk::QueryExtents"]
old-location: base\ivdsdisk_queryextents.htm
tech.root: base
ms.assetid: 2e7de42f-da7a-41a7-b38e-849ab8d72ab2
ms.date: 12/05/2018
ms.keywords: IVdsDisk interface [VDS],QueryExtents method, IVdsDisk.QueryExtents, IVdsDisk::QueryExtents, QueryExtents, QueryExtents method [VDS], QueryExtents method [VDS],IVdsDisk interface, base.ivdsdisk_queryextents, vds/IVdsDisk::QueryExtents
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
 - IVdsDisk::QueryExtents
 - vds/IVdsDisk::QueryExtents
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
 - IVdsDisk.QueryExtents
---

# IVdsDisk::QueryExtents


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the details 
   of all the extents on a disk.

## -parameters

### -param ppExtentArray [out]

A pointer variable that receives an  
      array of <a href="/windows/desktop/api/vds/ns-vds-vds_disk_extent">VDS_DISK_EXTENT</a> structures. 
      Callers must free this array by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfExtents [out]

The address of a type <b>LONG</b> representing the total number of extents.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The extent information was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PACK_OFFLINE</b></dt>
<dt>0x80042444L</dt>
</dl>
</td>
<td width="60%">
The pack to which the disk belongs is inaccessible.

</td>
</tr>
</table>

## -remarks

Use this method to determine the amount of available free space for creating or extending volumes. You can 
    also use the extent information to determine how many volumes occupy the disk. Valid extent types are: unknown 
    extents, free extents, data extents, OEM extents, ESP extents, MSR extents, LDM metadata extents, and unusable 
    extents. A data extent contains a link to the volume on top of it.

If the disk is a dynamic disk, it must be online. If it is a basic disk or a raw disk, it can be online or offline.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdisk">IVdsDisk</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-clearflags">IVdsDisk::ClearFlags</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-convertstyle">IVdsDisk::ConvertStyle</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getidentificationdata">IVdsDisk::GetIdentificationData</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getpack">IVdsDisk::GetPack</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-setflags">IVdsDisk::SetFlags</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_extent">VDS_DISK_EXTENT</a>