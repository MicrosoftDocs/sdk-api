---
UID: NF:vds.IVdsSubSystemImportTarget.GetImportTarget
title: IVdsSubSystemImportTarget::GetImportTarget (vds.h)
description: Returns the Volume Shadow Copy service (VSS) import target for the computer for this subsystem.
helpviewer_keywords: ["GetImportTarget","GetImportTarget method [VDS]","GetImportTarget method [VDS]","IVdsSubSystemImportTarget interface","IVdsSubSystemImportTarget interface [VDS]","GetImportTarget method","IVdsSubSystemImportTarget.GetImportTarget","IVdsSubSystemImportTarget::GetImportTarget","base.ivdssubsystemimporttarget_getimporttarget","vds/IVdsSubSystemImportTarget::GetImportTarget"]
old-location: base\ivdssubsystemimporttarget_getimporttarget.htm
tech.root: base
ms.assetid: 1fff1400-61d9-494f-857d-53626b80c2d2
ms.date: 12/05/2018
ms.keywords: GetImportTarget, GetImportTarget method [VDS], GetImportTarget method [VDS],IVdsSubSystemImportTarget interface, IVdsSubSystemImportTarget interface [VDS],GetImportTarget method, IVdsSubSystemImportTarget.GetImportTarget, IVdsSubSystemImportTarget::GetImportTarget, base.ivdssubsystemimporttarget_getimporttarget, vds/IVdsSubSystemImportTarget::GetImportTarget
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
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsSubSystemImportTarget::GetImportTarget
 - vds/IVdsSubSystemImportTarget::GetImportTarget
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
 - IVdsSubSystemImportTarget.GetImportTarget
---

# IVdsSubSystemImportTarget::GetImportTarget


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the Volume Shadow Copy service (VSS) import target for the computer for this subsystem. Whenever shadow copies are created and a LUN from a shadow copy set from the subsystem is imported onto this computer, it will be 
   associated with the import target by the VSS hardware provider.

## -parameters

### -param ppwszIscsiName [out]

The address of a pointer to a string. On successful return of this method, the string pointed to will 
      contain the import target iSCSI name. This string is initialized by VDS and must be freed by the caller using 
      the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

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
The import target was retrieved successfully.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
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
The subsystem object is no longer present.

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
The operation or combination of parameters is not supported by this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_IMPORT_TARGET</b></dt>
<dt>0x80042713L</dt>
</dl>
</td>
<td width="60%">
No import target was set for this subsystem.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdssubsystemimporttarget">IVdsSubSystemImportTarget</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdssubsystemimporttarget-setimporttarget">SetImportTarget</a>