---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IVdsServiceLoader::LoadService


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Launches VDS on the specified computer and returns a pointer to the service object.


## -parameters




### -param pwszMachineName [in]

This parameter must be set to <b>NULL</b>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This parameter contains the name of the host computer. Setting it to <b>NULL</b> causes VDS to be loaded and initialized on the local host.


### -param ppService [out]

The address of an <a href="https://msdn.microsoft.com/6b081cc8-fe06-427f-b06d-831a1f1fef52">IVdsService</a>
        interface pointer. Callers must release the interface when it is no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The service has launched successfully.

</td>
</tr>
</table>
 




## -remarks



Although <b>S_OK</b> indicates that VDS has launched successfully, the service initialization can be incomplete when the method returns. For this reason, after calling this method, you must call the <a href="https://msdn.microsoft.com/85075abe-7fac-40aa-a93e-19d89c0fd760">IVdsService::WaitForServiceReady</a> method to wait for VDS initialization to complete.

For a code example, see <a href="https://msdn.microsoft.com/6b75fdb2-3d4c-4419-96e8-8677439e366b">Loading VDS</a>.




## -see-also




<a href="https://msdn.microsoft.com/6b081cc8-fe06-427f-b06d-831a1f1fef52">IVdsService</a>



<a href="https://msdn.microsoft.com/85075abe-7fac-40aa-a93e-19d89c0fd760">IVdsService::WaitForServiceReady</a>



<a href="https://msdn.microsoft.com/43533ee7-4e44-48c9-8c9d-0992426d79ba">IVdsServiceLoader</a>
 

 

