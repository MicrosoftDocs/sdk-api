---
UID: NF:vds.IVdsIscsiPortal.SetStatus
title: IVdsIscsiPortal::SetStatus (vds.h)
description: The IVdsIscsiPortal::SetStatus method (vds.h) sets the status of a portal to the specified value.
helpviewer_keywords: ["IVdsIscsiPortal interface [VDS]","SetStatus method","IVdsIscsiPortal.SetStatus","IVdsIscsiPortal::SetStatus","SetStatus","SetStatus method [VDS]","SetStatus method [VDS]","IVdsIscsiPortal interface","base.ivdsiscsiportal_setstatus","vds/IVdsIscsiPortal::SetStatus","vdshwprv/IVdsIscsiPortal::SetStatus"]
old-location: base\ivdsiscsiportal_setstatus.htm
tech.root: base
ms.assetid: 6c63fa36-bccb-4731-999a-c6f8b565b38f
ms.date: 08/05/2022
ms.keywords: IVdsIscsiPortal interface [VDS],SetStatus method, IVdsIscsiPortal.SetStatus, IVdsIscsiPortal::SetStatus, SetStatus, SetStatus method [VDS], SetStatus method [VDS],IVdsIscsiPortal interface, base.ivdsiscsiportal_setstatus, vds/IVdsIscsiPortal::SetStatus, vdshwprv/IVdsIscsiPortal::SetStatus
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
 - IVdsIscsiPortal::SetStatus
 - vds/IVdsIscsiPortal::SetStatus
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
 - IVdsIscsiPortal.SetStatus
---

# IVdsIscsiPortal::SetStatus


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Not supported.

Sets the status of a portal to the specified value.

## -parameters

### -param status [in]

Values enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_portal_status">VDS_ISCSI_PORTAL_STATUS</a>. 
      Only <b>VDS_IPS_ONLINE</b> and <b>VDS_IPS_OFFLINE</b> enumeration values 
      are supported; the remaining values are only to be used by a provider to report status.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The status  was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
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
</dl>
</td>
<td width="60%">
The portal object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until the previous operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsiportal">IVdsIscsiPortal</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_portal_status">VDS_ISCSI_PORTAL_STATUS</a>
