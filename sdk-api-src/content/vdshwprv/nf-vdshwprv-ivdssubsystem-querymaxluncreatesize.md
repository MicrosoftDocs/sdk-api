---
UID: NF:vdshwprv.IVdsSubSystem.QueryMaxLunCreateSize
title: IVdsSubSystem::QueryMaxLunCreateSize (vdshwprv.h)
description: The IVdsSubSystem::QueryMaxLunCreateSize (vdshwprv.h) method returns the size of the maximum LUN that can be created using the specified LUN type and hints.
helpviewer_keywords: ["IVdsSubSystem interface","QueryMaxLunCreateSize method","IVdsSubSystem.QueryMaxLunCreateSize","IVdsSubSystem::QueryMaxLunCreateSize","QueryMaxLunCreateSize","QueryMaxLunCreateSize method","QueryMaxLunCreateSize method","IVdsSubSystem interface","base.ivdssubsystem_querymaxluncreatesize","vds/IVdsSubSystem::QueryMaxLunCreateSize","vdshwprv/IVdsSubSystem::QueryMaxLunCreateSize"]
old-location: base\ivdssubsystem_querymaxluncreatesize.htm
tech.root: base
ms.assetid: 16e8bcab-d01f-494a-9705-8392cf043674
ms.date: 08/08/2022
ms.keywords: IVdsSubSystem interface,QueryMaxLunCreateSize method, IVdsSubSystem.QueryMaxLunCreateSize, IVdsSubSystem::QueryMaxLunCreateSize, QueryMaxLunCreateSize, QueryMaxLunCreateSize method, QueryMaxLunCreateSize method,IVdsSubSystem interface, base.ivdssubsystem_querymaxluncreatesize, vds/IVdsSubSystem::QueryMaxLunCreateSize, vdshwprv/IVdsSubSystem::QueryMaxLunCreateSize
req.header: vdshwprv.h
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
 - IVdsSubSystem::QueryMaxLunCreateSize
 - vdshwprv/IVdsSubSystem::QueryMaxLunCreateSize
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
 - IVdsSubSystem.QueryMaxLunCreateSize
---

# IVdsSubSystem::QueryMaxLunCreateSize


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the size of the maximum LUN that can be created using the specified LUN type and hints.

## -parameters

### -param type [in]

The LUN type enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a>.

### -param pDriveIdArray [in]

A pointer to an array containing a <b>VDS_OBJECT_ID</b> for each of the drives to be 
      used in the LUN creation. The provider should attempt to use the drives in the order provided. This parameter 
      can be <b>NULL</b> if the <i>lNumberOfDrives</i> parameter is 0, in which 
      case the provider should automatically pick drives.

### -param lNumberOfDrives [in]

The number of entries in <i>pDriveIdArray</i>. This can be set to 0.

### -param pHints [in]

A pointer to the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure used for creating the LUN. The 
      hints always take lower priority than parameters listed before. This argument must be non-NULL.

### -param pullMaxLunSize [out]

A pointer to a buffer containing the maximum size of the LUN in bytes. This argument must be non-NULL.

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
This return value signals a software or communication problem inside a provider that caches information 
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
Can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant. This 
        return value indicates that the identifier does not refer to an existing object.

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

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem">IVdsSubSystem</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_type">VDS_LUN_TYPE</a>
