---
UID: NF:windows.devices.alljoyn.interop.IWindowsDevicesAllJoynBusAttachmentInterop.get_Win32Handle
title: IWindowsDevicesAllJoynBusAttachmentInterop::alljoyn
author: windows-driver-content
description: Classic COM interface that simply returns a pointer to the underlying alljoyn_busattachment instance, so the app can use it directly with the AllJoyn Core C API.
old-location: alljoyn\iwindowsdevicesalljoynbusattachmentinterop_get_win32handle.htm
old-project: AllJoyn
ms.assetid: E46C47FC-08D2-4CE6-9205-46A840DFA3F4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IInspectable ::get_Win32Handle, IInspectable interface [AllJoyn API],get_Win32Handle method, IWindowsDevicesAllJoynBusAttachmentInterop interface [AllJoyn API],get_Win32Handle method, IWindowsDevicesAllJoynBusAttachmentInterop.alljoyn, IWindowsDevicesAllJoynBusAttachmentInterop.get_Win32Handle, IWindowsDevicesAllJoynBusAttachmentInterop::alljoyn, IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle, alljoyn.iwindowsdevicesalljoynbusattachmentinterop_get_win32handle, get_Win32Handle, get_Win32Handle method [AllJoyn API], get_Win32Handle method [AllJoyn API],IInspectable interface, get_Win32Handle method [AllJoyn API],IWindowsDevicesAllJoynBusAttachmentInterop interface, windows/IInspectable ::get_Win32Handle, windows/IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PDF_RENDER_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	windows.devices.alljoyn.interop.h
api_name:
-	IWindowsDevicesAllJoynBusAttachmentInterop.get_Win32Handle
-	IInspectable .get_Win32Handle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWindowsDevicesAllJoynBusAttachmentInterop::alljoyn


## -description


Classic COM interface that simply returns a pointer to the underlying <b>alljoyn_busattachment</b> instance, so the app can use it directly with the AllJoyn Core C API.


## -parameters




### -param value [out]

The pointer to the underlying alljoyn_busattachment instance.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code. 





## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable </a>



<a href="https://msdn.microsoft.com/F08A2D95-A84E-47C9-9485-98306993DB52">IWindowsDevicesAllJoynBusAttachmentInterop</a>
 

 

