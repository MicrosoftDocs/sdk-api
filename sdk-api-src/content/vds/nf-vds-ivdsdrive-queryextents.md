---
UID: NF:vds.IVdsDrive.QueryExtents
title: IVdsDrive::QueryExtents (vds.h)
description: The IVdsDrive::QueryExtents method (vds.h) returns an array of the extents on a drive, including both allocated and unallocated extents.
helpviewer_keywords: ["IVdsDrive interface [VDS]","QueryExtents method","IVdsDrive.QueryExtents","IVdsDrive::QueryExtents","QueryExtents","QueryExtents method [VDS]","QueryExtents method [VDS]","IVdsDrive interface","base.ivdsdrive_queryextents","vds/IVdsDrive::QueryExtents","vdshwprv/IVdsDrive::QueryExtents"]
old-location: base\ivdsdrive_queryextents.htm
tech.root: base
ms.assetid: 8ee3e085-ce69-457e-b652-bb9c45b7fdd8
ms.date: 08/05/2022
ms.keywords: IVdsDrive interface [VDS],QueryExtents method, IVdsDrive.QueryExtents, IVdsDrive::QueryExtents, QueryExtents, QueryExtents method [VDS], QueryExtents method [VDS],IVdsDrive interface, base.ivdsdrive_queryextents, vds/IVdsDrive::QueryExtents, vdshwprv/IVdsDrive::QueryExtents
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
 - IVdsDrive::QueryExtents
 - vds/IVdsDrive::QueryExtents
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
 - IVdsDrive.QueryExtents
---

# IVdsDrive::QueryExtents


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an array of 
   the extents on a drive, including both allocated and unallocated extents.

## -parameters

### -param ppExtentArray [out]

A pointer to the  array of <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_extent">VDS_DRIVE_EXTENT</a> structures passed in by the caller. Callers must free this array by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfExtents [out]

A pointer to the number of drive extents returned in the 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_extent">VDS_DRIVE_EXTENT</a> structure.

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
The extents information was returned successfully. For a drive without extents, the array is empty, the value 
        of <i>plNumberOfExtents</i> is set to 0, and the value of 
        <i>ppExtentArray</i> is set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information about 
        the array. Use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method
        followed by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The drive object no longer exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The drive is in a failed state, and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or operations 
        are complete.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
The subsystem does not support this method.

</td>
</tr>
</table>

## -remarks

A drive can contribute extents to any number of LUNs, and these LUNs can be unmasked to any number of different
    computers on the network. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a> method to see all 
    the extents of a LUN plex.

The <b>LunId</b> member of each 
     <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_extent">VDS_DRIVE_EXTENT</a> structure specifies the GUID for the LUN to which each allocated extent contributes. Consequently, you can use 
     the result of this method to determine the number of LUNs to which the drive contributes by counting the number 
     of distinct <b>LunId</b> values returned in <i>ppExtentArray</i>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsdrive">IVdsDrive</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-queryextents">IVdsLunPlex::QueryExtents</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_extent">VDS_DRIVE_EXTENT</a>
