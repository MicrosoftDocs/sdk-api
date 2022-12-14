---
UID: NF:vdshwprv.IVdsSubSystem2.GetProperties2
title: IVdsSubSystem2::GetProperties2 (vdshwprv.h)
description: The VdsSubSystem2::GetProperties2 (vdshwprv.h) method returns the properties of a subsystem.
helpviewer_keywords: ["GetProperties2","GetProperties2 method","GetProperties2 method","IVdsSubSystem2 interface","IVdsSubSystem2 interface","GetProperties2 method","IVdsSubSystem2.GetProperties2","IVdsSubSystem2::GetProperties2","base.ivdssubsystem2_getproperties2","vds/IVdsSubSystem2::GetProperties2","vdshwprv/IVdsSubSystem2::GetProperties2"]
old-location: base\ivdssubsystem2_getproperties2.htm
tech.root: base
ms.assetid: 1f2164a9-643d-4762-8a2e-31d5c277502e
ms.date: 08/08/2022
ms.keywords: GetProperties2, GetProperties2 method, GetProperties2 method,IVdsSubSystem2 interface, IVdsSubSystem2 interface,GetProperties2 method, IVdsSubSystem2.GetProperties2, IVdsSubSystem2::GetProperties2, base.ivdssubsystem2_getproperties2, vds/IVdsSubSystem2::GetProperties2, vdshwprv/IVdsSubSystem2::GetProperties2
req.header: vdshwprv.h
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
 - IVdsSubSystem2::GetProperties2
 - vdshwprv/IVdsSubSystem2::GetProperties2
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
 - IVdsSubSystem2.GetProperties2
---

# IVdsSubSystem2::GetProperties2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of a subsystem. This method is identical to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-getproperties">IVdsSubSystem::GetProperties</a> method, except that it returns a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop2">VDS_SUB_SYSTEM_PROP2</a> structure instead of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure.

## -parameters

### -param pSubSystemProp2 [out]

The address of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop2">VDS_SUB_SYSTEM_PROP2</a> 
      structure allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszFriendlyName</b> and <b>pwszIdentification</b> member strings. 
      Callers must free the strings by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

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
<dt><b><b>VDS_S_PROPERTIES_INCOMPLETE</b></b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

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
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem2">IVdsSubSystem2</a>
