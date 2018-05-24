---
UID: NF:vds.IVdsIscsiInitiatorAdapter.LoginToTarget
title: IVdsIscsiInitiatorAdapter::LoginToTarget
author: windows-driver-content
description: Performs a manual login to an iSCSI target.
old-location: base\ivdsiscsiinitiatoradapter_logintotarget.htm
old-project: VDS
ms.assetid: 74d6ddd0-1b78-446a-9bce-6816eb34a2b9
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVdsIscsiInitiatorAdapter interface [VDS],LoginToTarget method, IVdsIscsiInitiatorAdapter.LoginToTarget, IVdsIscsiInitiatorAdapter::LoginToTarget, LoginToTarget, LoginToTarget method [VDS], LoginToTarget method [VDS],IVdsIscsiInitiatorAdapter interface, base.ivdsiscsiinitiatoradapter_logintotarget, vds/IVdsIscsiInitiatorAdapter::LoginToTarget
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsIscsiInitiatorAdapter.LoginToTarget
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsIscsiInitiatorAdapter::LoginToTarget


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Performs a manual login to an iSCSI target.


## -parameters




### -param loginType [in]


      The type of login that will be performed, enumerated by 
      <a href="https://msdn.microsoft.com/d40db9ab-6fa5-4efb-83e8-ce1dce5fe0c2">VDS_ISCSI_LOGIN_TYPE</a>.


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


      Flags enumerated by <a href="https://msdn.microsoft.com/c315f5cc-2b15-4185-8d22-7114950273e7">VDS_ISCSI_LOGIN_FLAG</a> 
      specifying login options.


### -param bHeaderDigest [in]


      If <b>TRUE</b>, the initiator should enable header digest when logging into the target portal.


### -param bDataDigest [in]


      If <b>TRUE</b>, the initiator should enable data digest when logging into the target portal.


### -param authType [in]


      The type of authentication required to log into the target, enumerated by 
      <a href="https://msdn.microsoft.com/7e445b10-552a-4a89-aee8-9699db79c5a3">VDS_ISCSI_AUTH_TYPE</a>.


### -param ppAsync [out]


      The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface. Use this interface to cancel, wait 
      for, or query the status of the operation. If 
      <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> is called on this interface and a success HRESULT value is returned, the 
      interfaces returned in the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> 
      structure must be released by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="_com_succeeded">SUCCEEDED</a> and <a href="_com_failed">FAILED</a> macros defined in Winerror.h.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The login was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ISCSI_LOGIN_FAILED</b></b></dt>
<dt>0x80042708L</dt>
</dl>
</td>
<td width="60%">

        Another operation is in progress. This operation cannot proceed until the previous operations are complete.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/3f911878-28c6-41db-ae9c-81e282aabf9d">IVdsIscsiInitiatorAdapter</a>



<a href="https://msdn.microsoft.com/7e445b10-552a-4a89-aee8-9699db79c5a3">VDS_ISCSI_AUTH_TYPE</a>



<a href="https://msdn.microsoft.com/c315f5cc-2b15-4185-8d22-7114950273e7">VDS_ISCSI_LOGIN_FLAG</a>



<a href="https://msdn.microsoft.com/d40db9ab-6fa5-4efb-83e8-ce1dce5fe0c2">VDS_ISCSI_LOGIN_TYPE</a>
 

 

