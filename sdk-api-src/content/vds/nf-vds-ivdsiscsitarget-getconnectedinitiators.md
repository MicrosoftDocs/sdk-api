---
UID: NF:vds.IVdsIscsiTarget.GetConnectedInitiators
title: IVdsIscsiTarget::GetConnectedInitiators (vds.h)
description: The IVdsIscsiTarget::GetConnectedInitiators method (vds.h) returns the list of iSCSI names of the initiators currently logged into the target.
helpviewer_keywords: ["GetConnectedInitiators","GetConnectedInitiators method [VDS]","GetConnectedInitiators method [VDS]","IVdsIscsiTarget interface","IVdsIscsiTarget interface [VDS]","GetConnectedInitiators method","IVdsIscsiTarget.GetConnectedInitiators","IVdsIscsiTarget::GetConnectedInitiators","base.ivdsiscsitarget_getconnectedinitiators","vds/IVdsIscsiTarget::GetConnectedInitiators","vdshwprv/IVdsIscsiTarget::GetConnectedInitiators"]
old-location: base\ivdsiscsitarget_getconnectedinitiators.htm
tech.root: base
ms.assetid: 2060f012-169c-4077-a6ed-cef362f926d4
ms.date: 08/05/2022
ms.keywords: GetConnectedInitiators, GetConnectedInitiators method [VDS], GetConnectedInitiators method [VDS],IVdsIscsiTarget interface, IVdsIscsiTarget interface [VDS],GetConnectedInitiators method, IVdsIscsiTarget.GetConnectedInitiators, IVdsIscsiTarget::GetConnectedInitiators, base.ivdsiscsitarget_getconnectedinitiators, vds/IVdsIscsiTarget::GetConnectedInitiators, vdshwprv/IVdsIscsiTarget::GetConnectedInitiators
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
 - IVdsIscsiTarget::GetConnectedInitiators
 - vds/IVdsIscsiTarget::GetConnectedInitiators
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
 - IVdsIscsiTarget.GetConnectedInitiators
---

# IVdsIscsiTarget::GetConnectedInitiators


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the list of iSCSI names of the initiators currently logged into the 
   target.

## -parameters

### -param pppwszInitiatorList [out]

The address of a variable that receives an array of strings containing the iSCSI names of the initiators currently logged into the 
      target. Callers must free each string in this array, as well as the array itself, by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfInitiators [out]

A pointer to the number of strings returned in <i>pppwszInitiatorList</i>.

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
The list of connected initiators was returned successfully.

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
Another operation is in progress; this operation cannot proceed until the previous operations are 
        complete.

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
The target object is no longer present.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>
