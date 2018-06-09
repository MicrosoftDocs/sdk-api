---
UID: NF:vds.IVdsController.SetStatus
title: IVdsController::SetStatus
author: windows-sdk-content
description: Sets the status of a controller to the specified value.
old-location: base\ivdscontroller_setstatus.htm
old-project: VDS
ms.assetid: f9bae451-ef47-46ad-a11e-b7b36a031a8a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsController interface [VDS],SetStatus method, IVdsController.SetStatus, IVdsController::SetStatus, SetStatus, SetStatus method [VDS], SetStatus method [VDS],IVdsController interface, base.ivdscontroller_setstatus, vds/IVdsController::SetStatus, vdshwprv/IVdsController::SetStatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsController.SetStatus
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsController::SetStatus


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]


   Sets the status of a 
   controller to the specified value.
  


## -parameters




### -param status [in]


      Values enumerated by <a href="https://msdn.microsoft.com/a888fcb7-83f5-40c1-9f24-efa929aa9f6a">VDS_CONTROLLER_STATUS</a>. 
      Callers can pass in a subset of the possible enumeration values. Passing in 
      <b>VDS_CS_UNKNOWN</b> returns <b>E_INVALIDARG</b>.


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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">

        This return value signals a software or communication problem inside a provider that caches information about 
        the array. Use the <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> 
        method followed by the 
        <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> method to restore 
        the cache.
       

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
The controller object is no longer present.

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
The controller is in a failed state and is unable to perform the requested operation.

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

        Another operation is in progress; this operation cannot proceed until the previous operation or operations 
        are complete.
       

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
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>
 




## -remarks




    This method enables you to set the status of a single controller. You can set the status of all the controllers 
    in a subsystem at once by calling the 
    <a href="https://msdn.microsoft.com/080a48a5-1c25-440a-ad3c-528cdaef40e9">IVdsSubSystem::SetControllerStatus</a> 
    method. Use the 
    <a href="https://msdn.microsoft.com/37230ac4-45f5-46ba-9a1c-072409e9362c">IVdsController::GetProperties</a> 
    method to get the current status of the controller.
   


    Implementers are responsible for performing any necessary operations to get the status to the specified state. 
    For example, if the caller passes in <b>VDS_CS_OFFLINE</b> as the controller status, you might 
    need to first clear the cache for the controller.




## -see-also




<a href="https://msdn.microsoft.com/cc30a78a-78a4-49c2-a97d-228400da46a9">IVdsController</a>



<a href="https://msdn.microsoft.com/37230ac4-45f5-46ba-9a1c-072409e9362c">IVdsController::GetProperties</a>



<a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>



<a href="https://msdn.microsoft.com/080a48a5-1c25-440a-ad3c-528cdaef40e9">IVdsSubSystem::SetControllerStatus</a>



<a href="https://msdn.microsoft.com/a888fcb7-83f5-40c1-9f24-efa929aa9f6a">VDS_CONTROLLER_STATUS</a>
 

 

