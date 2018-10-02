---
UID: NF:vdshwprv.IVdsAdmin.UnregisterProvider
title: IVdsAdmin::UnregisterProvider
author: windows-sdk-content
description: Removes VDS provider registration data. Hardware providers call this method.
old-location: base\ivdsadmin_unregisterprovider.htm
tech.root: VDS
ms.assetid: da78b4ed-17e3-4953-9e5e-310e55349058
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsAdmin interface [VDS],UnregisterProvider method, IVdsAdmin.UnregisterProvider, IVdsAdmin::UnregisterProvider, UnregisterProvider, UnregisterProvider method [VDS], UnregisterProvider method [VDS],IVdsAdmin interface, base.ivdsadmin_unregisterprovider, vdshwprv/IVdsAdmin::UnregisterProvider
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVdsAdmin.UnregisterProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsAdmin::UnregisterProvider


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Removes VDS provider registration data. Hardware providers call this method.


## -parameters




### -param providerId

The GUID of the provider.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used.




## -remarks



An in-process provider calls this method from the 
    <a href="https://msdn.microsoft.com/en-us/library/ms682162(v=VS.85).aspx">DllRegisterServer</a> function; whereas, an out-of-process 
    provider calls from the 
    <a href="https://msdn.microsoft.com/en-us/library/ms633559(v=VS.85).aspx">WinMain</a> 
    function.




## -see-also




<a href="https://msdn.microsoft.com/693ee0c0-9f86-4f78-9724-f3a3420463c9">IVdsAdmin</a>



<a href="https://msdn.microsoft.com/bb6e0037-7f44-418d-897c-12bf15224841">IVdsAdmin::RegisterProvider</a>
 

 

