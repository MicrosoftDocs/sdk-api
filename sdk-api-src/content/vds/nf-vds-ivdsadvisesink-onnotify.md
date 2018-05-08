---
UID: NF:vds.IVdsAdviseSink.OnNotify
title: IVdsAdviseSink::OnNotify
author: windows-driver-content
description: Passes notifications from providers to VDS, and from VDS to applications.
old-location: base\ivdsadvisesink_onnotify.htm
old-project: VDS
ms.assetid: 0cf7bf55-922e-4092-bb2f-6423d9addb0c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IVdsAdviseSink interface [VDS],OnNotify method, IVdsAdviseSink.OnNotify, IVdsAdviseSink::OnNotify, OnNotify, OnNotify method [VDS], OnNotify method [VDS],IVdsAdviseSink interface, base.ivdsadvisesink_onnotify, vds/IVdsAdviseSink::OnNotify, vdshwprv/IVdsAdviseSink::OnNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
-	IVdsAdviseSink.OnNotify
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsAdviseSink::OnNotify


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Passes notifications 
   from providers to VDS, and from VDS to applications.


## -parameters




### -param lNumberOfNotifications [in]

The number of notifications specified in <i>pNotificationArray</i>.


### -param pNotificationArray [in]

A pointer to an array of <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> 
      structures. A provider allocates the memory for the array when the provider calls into the service; the 
      service frees the array. VDS allocates the array when the service calls into an application. In this case, 
      callers must free the array by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
VDS returns this value to a provider if the service is not fully initialized when the provider calls into 
        this method, or if some notifications are lost by the service.

</td>
</tr>
</table>
 




## -remarks



An application implements this method to receive notifications from VDS. Some of these notifications originate from VDS; others are provider notifications that are forwarded by VDS.

VDS maintains a cache of information about the properties of all VDS objects, such as subsystems and controllers. Whenever a change occurs that triggers a notification, this cache is updated automatically. Also, calling <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> or <a href="https://msdn.microsoft.com/ca6a1143-b5f0-49e5-8505-836c565aabcf">IVdsService::Refresh</a> in response to a VDS notification could cause an endless loop of notifications to be sent. For these reasons, an application should not call <b>IVdsHwProvider::Refresh</b> or <b>IVdsService::Refresh</b> in its implementation of this method. 

For providers that use this method to send notifications, it is good practice to group notifications originating from a single event together. For example, when a LUN 
    is deleted, send <b>VDS_NF_DRIVE_MODIFY</b> notifications for all affected drives 
    together.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/ca6a1143-b5f0-49e5-8505-836c565aabcf">IVdsService::Refresh</a>



<a href="https://msdn.microsoft.com/085d380c-2e09-470a-a23d-704c31535975">IVdsService::Unadvise</a>



<a href="https://msdn.microsoft.com/a0841215-3eb0-4769-b320-4da25b535362">VDS Notifications</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

