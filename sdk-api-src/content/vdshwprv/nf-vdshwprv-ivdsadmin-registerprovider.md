---
UID: NF:vdshwprv.IVdsAdmin.RegisterProvider
title: IVdsAdmin::RegisterProvider
author: windows-sdk-content
description: Registers the specified hardware provider with VDS. Hardware providers call this method.
old-location: base\ivdsadmin_registerprovider.htm
old-project: VDS
ms.assetid: bb6e0037-7f44-418d-897c-12bf15224841
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsAdmin interface [VDS],RegisterProvider method, IVdsAdmin.RegisterProvider, IVdsAdmin::RegisterProvider, RegisterProvider, RegisterProvider method [VDS], RegisterProvider method [VDS],IVdsAdmin interface, base.ivdsadmin_registerprovider, vdshwprv/IVdsAdmin::RegisterProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
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
 - IVdsAdmin.RegisterProvider
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
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



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
    <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a>; whereas, an out-of-process 
    provider calls from the 
    <a href="https://www.bing.com/search?q=WinMain">WinMain</a> 
    function.

Hardware providers must not stop running while VDS is running.




## -see-also




<a href="https://msdn.microsoft.com/693ee0c0-9f86-4f78-9724-f3a3420463c9">IVdsAdmin</a>



<a href="https://msdn.microsoft.com/da78b4ed-17e3-4953-9e5e-310e55349058">IVdsAdmin::UnregisterProvider</a>



<a href="https://msdn.microsoft.com/a794e054-1389-4b54-9ad3-eb32b9dd0a5b">VDS_PROVIDER_TYPE</a>
 

 

