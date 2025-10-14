---
UID: NF:vdshwprv.IVdsIscsiTarget.GetProperties
title: IVdsIscsiTarget::GetProperties (vdshwprv.h)
description: The IVdsIscsiTarget::GetProperties (vdshwprv.h) method returns the properties of an iSCSI target.
helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsIscsiTarget interface","IVdsIscsiTarget interface [VDS]","GetProperties method","IVdsIscsiTarget.GetProperties","IVdsIscsiTarget::GetProperties","base.ivdsiscsitarget_getproperties","vds/IVdsIscsiTarget::GetProperties","vdshwprv/IVdsIscsiTarget::GetProperties"]
old-location: base\ivdsiscsitarget_getproperties.htm
tech.root: base
ms.assetid: db48ec8e-aae1-4b88-9942-6a23de2cfe25
ms.date: 08/08/2022
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsIscsiTarget interface, IVdsIscsiTarget interface [VDS],GetProperties method, IVdsIscsiTarget.GetProperties, IVdsIscsiTarget::GetProperties, base.ivdsiscsitarget_getproperties, vds/IVdsIscsiTarget::GetProperties, vdshwprv/IVdsIscsiTarget::GetProperties
req.header: vdshwprv.h
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
 - IVdsIscsiTarget::GetProperties
 - vdshwprv/IVdsIscsiTarget::GetProperties
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
 - IVdsIscsiTarget.GetProperties
---

# IVdsIscsiTarget::GetProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the properties of an iSCSI target.

## -parameters

### -param pTargetProp [out]

The address of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_target_prop">VDS_ISCSI_TARGET_PROP</a> 
      structure allocated by the caller. VDS allocates memory for the strings pointed to by the 
      <b>pwszIscsiName</b> and <b>pwszFriendlyName</b> members of this 
      structure. Callers must free the strings by using the 
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The properties were returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_PROPERTIES_INCOMPLETE</b></dt>
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
The portal object is no longer present.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_target_prop">VDS_ISCSI_TARGET_PROP</a>
