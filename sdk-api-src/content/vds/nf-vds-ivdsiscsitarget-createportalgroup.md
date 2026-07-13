---
UID: NF:vds.IVdsIscsiTarget.CreatePortalGroup
title: IVdsIscsiTarget::CreatePortalGroup (vds.h)
description: The IVdsIscsiTarget::CreatePortalGroup method (vds.h) creates a portal group.
helpviewer_keywords: ["CreatePortalGroup","CreatePortalGroup method [VDS]","CreatePortalGroup method [VDS]","IVdsIscsiTarget interface","IVdsIscsiTarget interface [VDS]","CreatePortalGroup method","IVdsIscsiTarget.CreatePortalGroup","IVdsIscsiTarget::CreatePortalGroup","base.ivdsiscsitarget_createportalgroup","vds/IVdsIscsiTarget::CreatePortalGroup","vdshwprv/IVdsIscsiTarget::CreatePortalGroup"]
old-location: base\ivdsiscsitarget_createportalgroup.htm
tech.root: base
ms.assetid: c479b5ee-2e6a-4a3f-bd80-c3c25adac20f
ms.date: 08/05/2022
ms.keywords: CreatePortalGroup, CreatePortalGroup method [VDS], CreatePortalGroup method [VDS],IVdsIscsiTarget interface, IVdsIscsiTarget interface [VDS],CreatePortalGroup method, IVdsIscsiTarget.CreatePortalGroup, IVdsIscsiTarget::CreatePortalGroup, base.ivdsiscsitarget_createportalgroup, vds/IVdsIscsiTarget::CreatePortalGroup, vdshwprv/IVdsIscsiTarget::CreatePortalGroup
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
 - IVdsIscsiTarget::CreatePortalGroup
 - vds/IVdsIscsiTarget::CreatePortalGroup
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
 - IVdsIscsiTarget.CreatePortalGroup
---

# IVdsIscsiTarget::CreatePortalGroup


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates a portal group. The interface pointer for the new 
   portal group object can be retrieved by calling 
   <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> through the 
   <i>ppAsync</i> parameter. The 
   <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure returned contains the volume 
   object interface pointer in the <b>cpg.pPortalGroupUnk</b> member.

## -parameters

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, which VDS 
      initializes on return. Callers must release the interface. Use this interface to cancel, wait for, or query the 
      status of the operation. If you call the 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method on this interface and a success HRESULT value is returned, you must 
      release the interfaces returned in the 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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
The portal group was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_ALREADY_EXISTS</b></dt>
<dt>0x00042714L</dt>
</dl>
</td>
<td width="60%">
No more portal groups can be created. The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-createportalgroup">CreatePortalGroup</a> method did not create a new portal group. If you call the 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method on the interface pointer returned in the 
   <i>ppAsync</i> parameter, an existing portal group object is retrieved.

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
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>
