---
UID: NF:vds.IVdsSubSystemNaming.SetFriendlyName
title: IVdsSubSystemNaming::SetFriendlyName (vds.h)
description: The IVdsSubSystemNaming::SetFriendlyName method (vds.h) sets the friendly name of a subsystem.
helpviewer_keywords: ["IVdsSubSystemNaming interface","SetFriendlyName method","IVdsSubSystemNaming.SetFriendlyName","IVdsSubSystemNaming::SetFriendlyName","SetFriendlyName","SetFriendlyName method","SetFriendlyName method","IVdsSubSystemNaming interface","base.ivdssubsystemnaming_setfriendlyname","vds/IVdsSubSystemNaming::SetFriendlyName","vdshwprv/IVdsSubSystemNaming::SetFriendlyName"]
old-location: base\ivdssubsystemnaming_setfriendlyname.htm
tech.root: base
ms.assetid: 8356eb25-af8c-4643-9ac4-e4ce001b617c
ms.date: 08/08/2022
ms.keywords: IVdsSubSystemNaming interface,SetFriendlyName method, IVdsSubSystemNaming.SetFriendlyName, IVdsSubSystemNaming::SetFriendlyName, SetFriendlyName, SetFriendlyName method, SetFriendlyName method,IVdsSubSystemNaming interface, base.ivdssubsystemnaming_setfriendlyname, vds/IVdsSubSystemNaming::SetFriendlyName, vdshwprv/IVdsSubSystemNaming::SetFriendlyName
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsSubSystemNaming::SetFriendlyName
 - vds/IVdsSubSystemNaming::SetFriendlyName
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
 - IVdsSubSystemNaming.SetFriendlyName
---

# IVdsSubSystemNaming::SetFriendlyName


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the friendly name of a subsystem.

## -parameters

### -param pwszFriendlyName

A pointer to a null-terminated string specifying the name to assign to the subsystem.

## -returns

This method can return standard <b>HRESULT</b> values, such as <b>E_INVALIDARG</b> or <b>E_OUTOFMEMORY</b>, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The name was successfully set.

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
        was set might not match the name passed in the <i>pwszName</i> parameter.

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
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to 
        restore the cache.

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
Another operation is in progress. This operation cannot proceed until  previous operations are 
        complete.

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
This operation is not supported by this provider.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystemnaming">IVdsSubSystemNaming</a>
