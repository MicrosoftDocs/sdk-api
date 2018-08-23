---
UID: NF:vdshwprv.IVdsSubSystem.SetControllerStatus
title: IVdsSubSystem::SetControllerStatus
author: windows-sdk-content
description: Sets the status (either online or offline) of the controllers in the subsystem.
old-location: base\ivdssubsystem_setcontrollerstatus.htm
old-project: vds
ms.assetid: 080a48a5-1c25-440a-ad3c-528cdaef40e9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsSubSystem interface [VDS],SetControllerStatus method, IVdsSubSystem.SetControllerStatus, IVdsSubSystem::SetControllerStatus, SetControllerStatus, SetControllerStatus method [VDS], SetControllerStatus method [VDS],IVdsSubSystem interface, base.ivdssubsystem_setcontrollerstatus, vds/IVdsSubSystem::SetControllerStatus, vdshwprv/IVdsSubSystem::SetControllerStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.redist: 
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
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsSubSystem.SetControllerStatus
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSubSystem::SetControllerStatus


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Sets 
   the status (either online or offline) of the controllers in the subsystem.


## -parameters




### -param pOnlineControllerIdArray [in]

Pointer to an array of controller GUIDs. The provider sets these controllers to online. This array includes 
      controllers already set to online that are to remain so.


### -param lNumberOfOnlineControllers [in]

The number of controllers specified in 
     <i>pOnlineControllersArray</i>.


### -param pOfflineControllerIdArray [in]

Pointer to an array of controller GUIDs. The provider sets these controllers to offline. This array includes 
      controllers already set to offline that are to remain so.


### -param lNumberOfOfflineControllers [in]

The number of controllers specified in <i>pOfflineControllersArray</i>.


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
This return value signals a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
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
The subsystem object is no longer present.

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
The subsystem is in a failed state and is unable to perform the requested operation.

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
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
Can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant. This return 
        value indicates that the identifier does not refer to an existing object.

</td>
</tr>
</table>
 




## -remarks



This method enables a caller to set the status of all controllers at once. Use the 
    <a href="https://msdn.microsoft.com/f9bae451-ef47-46ad-a11e-b7b36a031a8a">IVdsController::SetStatus</a> method to set the 
    status of a single controller.

Callers must pass the complete set of controllers in either the <i>pOnlineControllerIdArray</i> 
    or <i>pOfflineControllerIdArray</i> parameter for each method call. The 
    <b>E_INVALIDARG</b> return value can indicate that not all controllers in the subsystem have 
    been specified in the arguments to this method.  
    The <b>SetControllerStatus</b> method requires that 
    all controllers in the subsystem be present in one of the two arrays supplied.




## -see-also




<a href="https://msdn.microsoft.com/f9bae451-ef47-46ad-a11e-b7b36a031a8a">IVdsController::SetStatus</a>



<a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>



<a href="https://msdn.microsoft.com/1f1b9735-216b-4bc5-a9b8-2d274827b2c8">IVdsSubSystem</a>
 

 

