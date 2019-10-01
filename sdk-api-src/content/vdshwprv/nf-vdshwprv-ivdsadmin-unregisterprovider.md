---
UID: NF:vdshwprv.IVdsAdmin.UnregisterProvider
title: IVdsAdmin::UnregisterProvider (vdshwprv.h)
author: windows-sdk-content
description: Removes VDS provider registration data. Hardware providers call this method.
old-location: base\ivdsadmin_unregisterprovider.htm
tech.root: VDS
ms.assetid: da78b4ed-17e3-4953-9e5e-310e55349058
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVdsAdmin interface [VDS],UnregisterProvider method, IVdsAdmin.UnregisterProvider, IVdsAdmin::UnregisterProvider, UnregisterProvider, UnregisterProvider method [VDS], UnregisterProvider method [VDS],IVdsAdmin interface, base.ivdsadmin_unregisterprovider, vdshwprv/IVdsAdmin::UnregisterProvider
ms.topic: method
f1_keywords: 
 - "vdshwprv/IVdsAdmin.UnregisterProvider"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAdmin::UnregisterProvider


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Removes VDS provider registration data. Hardware providers call this method.


## -parameters




### -param providerId

The GUID of the provider.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used.




## -remarks



An in-process provider calls this method from the 
    <a href="https://docs.microsoft.com/windows/desktop/api/olectl/nf-olectl-dllregisterserver">DllRegisterServer</a> function; whereas, an out-of-process 
    provider calls from the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-winmain">WinMain</a> 
    function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadmin">IVdsAdmin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsadmin-registerprovider">IVdsAdmin::RegisterProvider</a>
 

 

