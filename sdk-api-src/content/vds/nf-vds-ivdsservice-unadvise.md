---
UID: NF:vds.IVdsService.Unadvise
title: IVdsService::Unadvise
author: windows-sdk-content
description: Unregisters the caller's IVdsAdviseSink interface so that the caller no longer receives notifications from the VDS service.
old-location: base\ivdsservice_unadvise.htm
tech.root: vds
ms.assetid: 085d380c-2e09-470a-a23d-704c31535975
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsService interface [VDS],Unadvise method, IVdsService.Unadvise, IVdsService::Unadvise, Unadvise, Unadvise method [VDS], Unadvise method [VDS],IVdsService interface, base.ivdsservice_unadvise, vds/IVdsService::Unadvise
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
 - IVdsService.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsService::Unadvise


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Unregisters the caller's  <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface so that the caller no longer receives notifications from the VDS service.


## -parameters




### -param dwCookie [in]

The cookie that was returned by the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> method when the <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface was registered.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_BAD_COOKIE</b></dt>
<dt>0x80042411L</dt>
</dl>
</td>
<td width="60%">
The cookie does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize. If an application calls this method before the service finishes initializing, the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">Advise</a> method to register your VDS application's  <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface to receive notifications from VDS.  <b>Advise</b> returns a cookie, which you must pass back as a parameter to the <b>Unadvise</b> method.

<div class="alert"><b>Note</b>  An application that calls <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">Advise</a> must eventually call <b>Unadvise</b>. Ideally, it should call <b>Unadvise</b> as soon as it no longer needs to receive notifications.</div>
<div> </div>
The <b>Unadvise</b> method might not return immediately, because it waits for a lock to update the list of registered client applications and waits for the notification thread sending the client notifications to exit. If there are outstanding notifications to be sent to your application, the notification thread tries to send them before exiting.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/6b081cc8-fe06-427f-b06d-831a1f1fef52">IVdsService</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/a0841215-3eb0-4769-b320-4da25b535362">VDS Notifications</a>
 

 

