---
UID: NF:vds.IVdsIscsiInitiatorAdapter.LogoutFromTarget
title: IVdsIscsiInitiatorAdapter::LogoutFromTarget (vds.h)
author: windows-sdk-content
description: Performs a manual logout from an iSCSI target on all iSCSI sessions to the specified target.
old-location: base\ivdsiscsiinitiatoradapter_logoutfromtarget.htm
tech.root: VDS
ms.assetid: b2f7598c-c532-4b68-b581-40b3f5eed1bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsIscsiInitiatorAdapter interface [VDS],LogoutFromTarget method, IVdsIscsiInitiatorAdapter.LogoutFromTarget, IVdsIscsiInitiatorAdapter::LogoutFromTarget, LogoutFromTarget, LogoutFromTarget method [VDS], LogoutFromTarget method [VDS],IVdsIscsiInitiatorAdapter interface, base.ivdsiscsiinitiatoradapter_logoutfromtarget, vds/IVdsIscsiInitiatorAdapter::LogoutFromTarget
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiInitiatorAdapter::LogoutFromTarget


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Performs a manual logout from an iSCSI target on all iSCSI sessions to the specified target.


## -parameters




### -param targetId [in]

The <b>VDS_OBJECT_ID</b> of the target to logout from.


### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface. Use this interface to cancel, wait 
      for, or query the status of the operation. If 
      <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> is called on this interface and a success HRESULT value is returned, the 
      interfaces returned in the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> 
      structure must be released by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="https://msdn.microsoft.com/en-us/library/ms687197(v=VS.85).aspx">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/en-us/library/ms693474(v=VS.85).aspx">FAILED</a> macros defined in Winerror.h.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The portal group was successfully deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ISCSI_LOGOUT_FAILED</b></b></dt>
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
<dt><b><b>VDS_E_ISCSI_SESSION_NOT_FOUND</b></b></dt>
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
<dt><b><b>VDS_E_ISCSI_LOGOUT_INCOMPLETE</b></b></dt>
<dt>0x80042710L</dt>
</dl>
</td>
<td width="60%">
At least one session did not logout successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/3f911878-28c6-41db-ae9c-81e282aabf9d">IVdsIscsiInitiatorAdapter</a>
 

 

