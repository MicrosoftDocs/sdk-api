---
UID: NF:windows.devices.alljoyn.interop.IWindowsDevicesAllJoynBusAttachmentInterop.get_Win32Handle
title: IWindowsDevicesAllJoynBusAttachmentInterop::alljoyn (windows.devices.alljoyn.interop.h)
description: Classic COM interface that simply returns a pointer to the underlying alljoyn_busattachment instance, so the app can use it directly with the AllJoyn Core C API.
helpviewer_keywords: ["IInspectable ::get_Win32Handle","IInspectable interface [AllJoyn API]","get_Win32Handle method","IWindowsDevicesAllJoynBusAttachmentInterop interface [AllJoyn API]","get_Win32Handle method","IWindowsDevicesAllJoynBusAttachmentInterop.alljoyn","IWindowsDevicesAllJoynBusAttachmentInterop.get_Win32Handle","IWindowsDevicesAllJoynBusAttachmentInterop::alljoyn","IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle","alljoyn.iwindowsdevicesalljoynbusattachmentinterop_get_win32handle","get_Win32Handle","get_Win32Handle method [AllJoyn API]","get_Win32Handle method [AllJoyn API]","IInspectable interface","get_Win32Handle method [AllJoyn API]","IWindowsDevicesAllJoynBusAttachmentInterop interface","windows/IInspectable ::get_Win32Handle","windows/IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle"]
old-location: alljoyn\iwindowsdevicesalljoynbusattachmentinterop_get_win32handle.htm
tech.root: AllJoyn
ms.assetid: E46C47FC-08D2-4CE6-9205-46A840DFA3F4
ms.date: 12/05/2018
ms.keywords: IInspectable ::get_Win32Handle, IInspectable interface [AllJoyn API],get_Win32Handle method, IWindowsDevicesAllJoynBusAttachmentInterop interface [AllJoyn API],get_Win32Handle method, IWindowsDevicesAllJoynBusAttachmentInterop.alljoyn, IWindowsDevicesAllJoynBusAttachmentInterop.get_Win32Handle, IWindowsDevicesAllJoynBusAttachmentInterop::alljoyn, IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle, alljoyn.iwindowsdevicesalljoynbusattachmentinterop_get_win32handle, get_Win32Handle, get_Win32Handle method [AllJoyn API], get_Win32Handle method [AllJoyn API],IInspectable interface, get_Win32Handle method [AllJoyn API],IWindowsDevicesAllJoynBusAttachmentInterop interface, windows/IInspectable ::get_Win32Handle, windows/IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle
 - windows.devices.alljoyn.interop/IWindowsDevicesAllJoynBusAttachmentInterop::get_Win32Handle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.devices.alljoyn.interop.h
api_name:
 - IWindowsDevicesAllJoynBusAttachmentInterop.get_Win32Handle
 - IInspectable .get_Win32Handle
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

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable </a>



<a href="/previous-versions/windows/desktop/api/windows.devices.alljoyn.interop/nn-windows-devices-alljoyn-interop-iwindowsdevicesalljoynbusattachmentinterop">IWindowsDevicesAllJoynBusAttachmentInterop</a>