---
UID: NF:windows.devices.alljoyn.interop.IWindowsDevicesAllJoynBusAttachmentFactoryInterop.CreateFromWin32Handle
title: IWindowsDevicesAllJoynBusAttachmentFactoryInterop::alljoyn (windows.devices.alljoyn.interop.h)
author: windows-sdk-content
description: Constructs an AllJoynBusAttachment over an existing alljoyn_busattachment instance without taking ownership.
old-location: alljoyn\iwindowsdevicesalljoynbusattachmentfactoryinterop_createfromwin32handle.htm
tech.root: AllJoyn
ms.assetid: AB33FA90-7A74-4B0D-8E99-EF304E508FCB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFromWin32Handle, CreateFromWin32Handle method [AllJoyn API], CreateFromWin32Handle method [AllJoyn API],IInspectable interface, CreateFromWin32Handle method [AllJoyn API],IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface, IInspectable ::CreateFromWin32Handle, IInspectable interface [AllJoyn API],CreateFromWin32Handle method, IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface [AllJoyn API],CreateFromWin32Handle method, IWindowsDevicesAllJoynBusAttachmentFactoryInterop.CreateFromWin32Handle, IWindowsDevicesAllJoynBusAttachmentFactoryInterop.alljoyn, IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle, IWindowsDevicesAllJoynBusAttachmentFactoryInterop::alljoyn, alljoyn.iwindowsdevicesalljoynbusattachmentfactoryinterop_createfromwin32handle, windows/IInspectable ::CreateFromWin32Handle, windows/IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle
ms.topic: method
req.header: windows.devices.alljoyn.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.devices.alljoyn.interop.h
api_name:
 - IWindowsDevicesAllJoynBusAttachmentFactoryInterop.CreateFromWin32Handle
 - IInspectable .CreateFromWin32Handle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsDevicesAllJoynBusAttachmentFactoryInterop::alljoyn


## -description


Constructs an <b>AllJoynBusAttachment</b> over an existing <b>alljoyn_busattachment</b> instance without taking ownership.


## -parameters




### -param win32handle [in]

The Win32 handle for the existing instance.


### -param enableAboutData [in]

Toggle to enable AboutData. 


### -param riid [in]

The ID of the <b>IAllJoynBusAttachment</b> interface.


### -param ppv [out]

Out parameter through which the  <b>AllJoynBusAttachment</b> is returned.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code. 




## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable </a>



<a href="https://msdn.microsoft.com/2E9FE6B4-E8F0-4627-A712-F7A4CE5404BE">IWindowsDevicesAllJoynBusAttachmentFactoryInterop</a>
 

 

