---
UID: NF:vds.IVdsSubSystem2.QueryMaxLunCreateSize2
title: IVdsSubSystem2::QueryMaxLunCreateSize2 (vds.h)
description: Returns the size of the maximum LUN that can be created using the specified LUN type and hints.
helpviewer_keywords: ["IVdsSubSystem2 interface","QueryMaxLunCreateSize2 method","IVdsSubSystem2.QueryMaxLunCreateSize2","IVdsSubSystem2::QueryMaxLunCreateSize2","QueryMaxLunCreateSize2","QueryMaxLunCreateSize2 method","QueryMaxLunCreateSize2 method","IVdsSubSystem2 interface","base.ivdssubsystem2_querymaxluncreatesize2","vds/IVdsSubSystem2::QueryMaxLunCreateSize2","vdshwprv/IVdsSubSystem2::QueryMaxLunCreateSize2"]
old-location: base\ivdssubsystem2_querymaxluncreatesize2.htm
tech.root: base
ms.assetid: 6cd892d2-f1b0-40cd-b037-5c670da3b32f
ms.date: 12/05/2018
ms.keywords: IVdsSubSystem2 interface,QueryMaxLunCreateSize2 method, IVdsSubSystem2.QueryMaxLunCreateSize2, IVdsSubSystem2::QueryMaxLunCreateSize2, QueryMaxLunCreateSize2, QueryMaxLunCreateSize2 method, QueryMaxLunCreateSize2 method,IVdsSubSystem2 interface, base.ivdssubsystem2_querymaxluncreatesize2, vds/IVdsSubSystem2::QueryMaxLunCreateSize2, vdshwprv/IVdsSubSystem2::QueryMaxLunCreateSize2
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
 - IVdsSubSystem2::QueryMaxLunCreateSize2
 - vds/IVdsSubSystem2::QueryMaxLunCreateSize2
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
 - IVdsSubSystem2.QueryMaxLunCreateSize2
---

# IVdsSubSystem2::QueryMaxLunCreateSize2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the size of the maximum LUN that can be created using the specified LUN type and hints. This method is identical to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-querymaxluncreatesize">IVdsSubSystem::QueryMaxLunCreateSize</a> method, except that the automagic hints are provided using a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure instead of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure.

## -parameters

### -param type [in]

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a> enumeration value that specifies the LUN type.

### -param pDriveIdArray [in]

A pointer to an array containing a <b>VDS_OBJECT_ID</b> for each of the drives to be 
      used in the LUN creation. The provider should attempt to use the drives in the order provided. This parameter 
      can be <b>NULL</b> if the <i>lNumberOfDrives</i> parameter is zero, in which 
      case the provider should automatically select drives.

### -param lNumberOfDrives [in]

The number of entries in the <i>pDriveIdArray</i> array. This parameter is optional and can be zero.

### -param pHints2 [in]

A pointer to the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure used for creating the LUN. The 
      hints always take lower priority than parameters listed before. This parameter is required and cannot be <b>NULL</b>.

### -param pullMaxLunSize [out]

A pointer to a buffer containing the maximum size of the LUN in bytes. This parameter is required and cannot be <b>NULL</b>.

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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
There is a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore 
        the cache.
       

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
The subsystem object is no longer present.

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
The subsystem is in a failed state and is unable to perform the requested operation.

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
Another operation is in progress; this operation cannot proceed until the previous operation or 
        operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The identifier does not refer to an existing object. This value can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant.

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
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem2">IVdsSubSystem2</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a>