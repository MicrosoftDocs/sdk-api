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

# IVdsAdmin::RegisterProvider


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Registers 
   the specified hardware provider with VDS. Hardware providers call this method.


## -parameters




### -param providerId [in]

The GUID of the hardware provider.


### -param providerClsid [in]

The COM class identifier (Clsid) of the hardware provider.


### -param pwszName [in]

The name of the hardware provider as  a zero-terminated, human-readable string.


### -param type [in]

The provider types enumerated by <a href="https://msdn.microsoft.com/a794e054-1389-4b54-9ad3-eb32b9dd0a5b">VDS_PROVIDER_TYPE</a>. 
     Use the <b>VDS_PT_HARDWARE</b> value to register a hardware provider with VDS.


### -param pwszMachineName [in]

The name of the computer on which the hardware provider executes; a null-terminated, human-readable string. 
     Use <b>NULL</b> to reference the current computer.


### -param pwszVersion [in]

The  version of the provider as a zero-terminated, human-readable string.


### -param guidVersionId [in]

The GUID for this version of the provider.


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
<dt><b>VDS_E_ALREADY_REGISTERED</b></dt>
<dt>0x80042403L</dt>
</dl>
</td>
<td width="60%">
The <i>providerId</i> is already registered. Only one version of a provider can be 
       registered at any given time.

</td>
</tr>
</table>
 




## -remarks



If necessary, call 
    <a href="https://msdn.microsoft.com/da78b4ed-17e3-4953-9e5e-310e55349058">UnregisterProvider</a> to remove a provider 
    before registering a new version.

An in-process provider calls this method from 
    <a href="_com_dllregisterserver">DllRegisterServer</a>; whereas, an out-of-process 
    provider calls from the 
    <a href="_win32_winmain_cpp">WinMain</a> 
    function.

Hardware providers must not stop running while VDS is running.




## -see-also




<a href="https://msdn.microsoft.com/693ee0c0-9f86-4f78-9724-f3a3420463c9">IVdsAdmin</a>



<a href="https://msdn.microsoft.com/da78b4ed-17e3-4953-9e5e-310e55349058">IVdsAdmin::UnregisterProvider</a>



<a href="https://msdn.microsoft.com/a794e054-1389-4b54-9ad3-eb32b9dd0a5b">VDS_PROVIDER_TYPE</a>
 

 

