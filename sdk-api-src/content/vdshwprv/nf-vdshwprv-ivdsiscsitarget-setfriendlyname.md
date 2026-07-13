---
UID: NF:vdshwprv.IVdsIscsiTarget.SetFriendlyName
title: IVdsIscsiTarget::SetFriendlyName (vdshwprv.h)
description: The IVdsIscsiTarget::SetFriendlyName (vdshwprv.h) method sets the friendly name of the target.
helpviewer_keywords: ["IVdsIscsiTarget interface [VDS]","SetFriendlyName method","IVdsIscsiTarget.SetFriendlyName","IVdsIscsiTarget::SetFriendlyName","SetFriendlyName","SetFriendlyName method [VDS]","SetFriendlyName method [VDS]","IVdsIscsiTarget interface","base.ivdsiscsitarget_setfriendlyname","vds/IVdsIscsiTarget::SetFriendlyName","vdshwprv/IVdsIscsiTarget::SetFriendlyName"]
old-location: base\ivdsiscsitarget_setfriendlyname.htm
tech.root: base
ms.assetid: 34afd8d7-473b-49c5-8486-2749144aea5c
ms.date: 08/08/2022
ms.keywords: IVdsIscsiTarget interface [VDS],SetFriendlyName method, IVdsIscsiTarget.SetFriendlyName, IVdsIscsiTarget::SetFriendlyName, SetFriendlyName, SetFriendlyName method [VDS], SetFriendlyName method [VDS],IVdsIscsiTarget interface, base.ivdsiscsitarget_setfriendlyname, vds/IVdsIscsiTarget::SetFriendlyName, vdshwprv/IVdsIscsiTarget::SetFriendlyName
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
 - IVdsIscsiTarget::SetFriendlyName
 - vdshwprv/IVdsIscsiTarget::SetFriendlyName
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
 - IVdsIscsiTarget.SetFriendlyName
---

# IVdsIscsiTarget::SetFriendlyName


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the friendly name of the target.

## -parameters

### -param pwszFriendlyName [in]

A string specifying the friendly name to assign to the target. This corresponds to the iSCSI alias.

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
The friendly name was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_NAME_TRUNCATED</b></dt>
<dt>0x00042700L</dt>
</dl>
</td>
<td width="60%">
The name was set successfully but had to be truncated due to limitations in the subsystem. The name that 
        was set might not match the name passed in the <i>pwszFriendlyName</i> parameter.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
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
The target object is no longer present.

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
Another operation is in progress; this operation cannot proceed until the previous operations are complete.

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

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>
