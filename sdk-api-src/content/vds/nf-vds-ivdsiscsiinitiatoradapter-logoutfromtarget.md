---
UID: NF:vds.IVdsIscsiInitiatorAdapter.LogoutFromTarget
title: IVdsIscsiInitiatorAdapter::LogoutFromTarget (vds.h)
description: Performs a manual logout from an iSCSI target on all iSCSI sessions to the specified target.
helpviewer_keywords: ["IVdsIscsiInitiatorAdapter interface [VDS]","LogoutFromTarget method","IVdsIscsiInitiatorAdapter.LogoutFromTarget","IVdsIscsiInitiatorAdapter::LogoutFromTarget","LogoutFromTarget","LogoutFromTarget method [VDS]","LogoutFromTarget method [VDS]","IVdsIscsiInitiatorAdapter interface","base.ivdsiscsiinitiatoradapter_logoutfromtarget","vds/IVdsIscsiInitiatorAdapter::LogoutFromTarget"]
old-location: base\ivdsiscsiinitiatoradapter_logoutfromtarget.htm
tech.root: base
ms.assetid: b2f7598c-c532-4b68-b581-40b3f5eed1bf
ms.date: 12/05/2018
ms.keywords: IVdsIscsiInitiatorAdapter interface [VDS],LogoutFromTarget method, IVdsIscsiInitiatorAdapter.LogoutFromTarget, IVdsIscsiInitiatorAdapter::LogoutFromTarget, LogoutFromTarget, LogoutFromTarget method [VDS], LogoutFromTarget method [VDS],IVdsIscsiInitiatorAdapter interface, base.ivdsiscsiinitiatoradapter_logoutfromtarget, vds/IVdsIscsiInitiatorAdapter::LogoutFromTarget
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
 - IVdsIscsiInitiatorAdapter::LogoutFromTarget
 - vds/IVdsIscsiInitiatorAdapter::LogoutFromTarget
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
 - IVdsIscsiInitiatorAdapter.LogoutFromTarget
---

# IVdsIscsiInitiatorAdapter::LogoutFromTarget


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Performs a manual logout from an iSCSI target on all iSCSI sessions to the specified target.

## -parameters

### -param targetId [in]

The <b>VDS_OBJECT_ID</b> of the target to logout from.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface. Use this interface to cancel, wait 
      for, or query the status of the operation. If 
      <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> is called on this interface and a success HRESULT value is returned, the 
      interfaces returned in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> 
      structure must be released by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros defined in Winerror.h.

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
The portal group was successfully deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ISCSI_LOGOUT_FAILED</b></dt>
<dt>0x80042709L</dt>
</dl>
</td>
<td width="60%">
The logout failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ISCSI_SESSION_NOT_FOUND</b></dt>
<dt>0x8004270AL</dt>
</dl>
</td>
<td width="60%">
VDS could not find a session matching the specified target.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ISCSI_LOGOUT_INCOMPLETE</b></dt>
<dt>0x80042710L</dt>
</dl>
</td>
<td width="60%">
At least one session did not logout successfully.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsiscsiinitiatoradapter">IVdsIscsiInitiatorAdapter</a>