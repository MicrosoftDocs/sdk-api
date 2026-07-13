---
UID: NF:vds.IVdsIscsiInitiatorAdapter.LoginToTarget
title: IVdsIscsiInitiatorAdapter::LoginToTarget (vds.h)
description: Performs a manual login to an iSCSI target.
helpviewer_keywords: ["IVdsIscsiInitiatorAdapter interface [VDS]","LoginToTarget method","IVdsIscsiInitiatorAdapter.LoginToTarget","IVdsIscsiInitiatorAdapter::LoginToTarget","LoginToTarget","LoginToTarget method [VDS]","LoginToTarget method [VDS]","IVdsIscsiInitiatorAdapter interface","base.ivdsiscsiinitiatoradapter_logintotarget","vds/IVdsIscsiInitiatorAdapter::LoginToTarget"]
old-location: base\ivdsiscsiinitiatoradapter_logintotarget.htm
tech.root: base
ms.assetid: 74d6ddd0-1b78-446a-9bce-6816eb34a2b9
ms.date: 12/05/2018
ms.keywords: IVdsIscsiInitiatorAdapter interface [VDS],LoginToTarget method, IVdsIscsiInitiatorAdapter.LoginToTarget, IVdsIscsiInitiatorAdapter::LoginToTarget, LoginToTarget, LoginToTarget method [VDS], LoginToTarget method [VDS],IVdsIscsiInitiatorAdapter interface, base.ivdsiscsiinitiatoradapter_logintotarget, vds/IVdsIscsiInitiatorAdapter::LoginToTarget
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
 - IVdsIscsiInitiatorAdapter::LoginToTarget
 - vds/IVdsIscsiInitiatorAdapter::LoginToTarget
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
 - IVdsIscsiInitiatorAdapter.LoginToTarget
---

# IVdsIscsiInitiatorAdapter::LoginToTarget


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Performs a manual login to an iSCSI target.

## -parameters

### -param loginType [in]

The type of login that will be performed, enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_login_type">VDS_ISCSI_LOGIN_TYPE</a>.

### -param targetId [in]

The <b>VDS_OBJECT_ID</b> of the target to login to. <b>GUID_NULL</b> 
      indicates that the initiator is to select the portal.

### -param targetPortalId [in]

The <b>VDS_OBJECT_ID</b> of the target portal by which the login operation is performed. 
      <b>GUID_NULL</b> indicates that the initiator is to select the portal.

### -param initiatorPortalId [in]

The <b>VDS_OBJECT_ID</b> of the initiator portal by which the login operation is 
      performed.

### -param ulLoginFlags [in]

Flags enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_login_flag">VDS_ISCSI_LOGIN_FLAG</a> 
      specifying login options.

### -param bHeaderDigest [in]

If <b>TRUE</b>, the initiator should enable header digest when logging into the target portal.

### -param bDataDigest [in]

If <b>TRUE</b>, the initiator should enable data digest when logging into the target portal.

### -param authType [in]

The type of authentication required to log into the target, enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_auth_type">VDS_ISCSI_AUTH_TYPE</a>.

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
The login was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ISCSI_LOGIN_FAILED</b></dt>
<dt>0x80042708L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until the previous operations are complete.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsiscsiinitiatoradapter">IVdsIscsiInitiatorAdapter</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_auth_type">VDS_ISCSI_AUTH_TYPE</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_login_flag">VDS_ISCSI_LOGIN_FLAG</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_iscsi_login_type">VDS_ISCSI_LOGIN_TYPE</a>