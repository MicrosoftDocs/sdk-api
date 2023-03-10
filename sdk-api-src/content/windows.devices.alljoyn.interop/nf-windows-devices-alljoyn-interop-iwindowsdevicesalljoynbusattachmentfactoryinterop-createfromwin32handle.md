---
UID: NF:windows.devices.alljoyn.interop.IWindowsDevicesAllJoynBusAttachmentFactoryInterop.CreateFromWin32Handle
title: IWindowsDevicesAllJoynBusAttachmentFactoryInterop::alljoyn (windows.devices.alljoyn.interop.h)
description: Constructs an AllJoynBusAttachment over an existing alljoyn_busattachment instance without taking ownership.
helpviewer_keywords: ["CreateFromWin32Handle","CreateFromWin32Handle method [AllJoyn API]","CreateFromWin32Handle method [AllJoyn API]","IInspectable interface","CreateFromWin32Handle method [AllJoyn API]","IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface","IInspectable ::CreateFromWin32Handle","IInspectable interface [AllJoyn API]","CreateFromWin32Handle method","IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface [AllJoyn API]","CreateFromWin32Handle method","IWindowsDevicesAllJoynBusAttachmentFactoryInterop.CreateFromWin32Handle","IWindowsDevicesAllJoynBusAttachmentFactoryInterop.alljoyn","IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle","IWindowsDevicesAllJoynBusAttachmentFactoryInterop::alljoyn","alljoyn.iwindowsdevicesalljoynbusattachmentfactoryinterop_createfromwin32handle","windows/IInspectable ::CreateFromWin32Handle","windows/IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle"]
old-location: alljoyn\iwindowsdevicesalljoynbusattachmentfactoryinterop_createfromwin32handle.htm
tech.root: AllJoyn
ms.assetid: AB33FA90-7A74-4B0D-8E99-EF304E508FCB
ms.date: 12/05/2018
ms.keywords: CreateFromWin32Handle, CreateFromWin32Handle method [AllJoyn API], CreateFromWin32Handle method [AllJoyn API],IInspectable interface, CreateFromWin32Handle method [AllJoyn API],IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface, IInspectable ::CreateFromWin32Handle, IInspectable interface [AllJoyn API],CreateFromWin32Handle method, IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface [AllJoyn API],CreateFromWin32Handle method, IWindowsDevicesAllJoynBusAttachmentFactoryInterop.CreateFromWin32Handle, IWindowsDevicesAllJoynBusAttachmentFactoryInterop.alljoyn, IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle, IWindowsDevicesAllJoynBusAttachmentFactoryInterop::alljoyn, alljoyn.iwindowsdevicesalljoynbusattachmentfactoryinterop_createfromwin32handle, windows/IInspectable ::CreateFromWin32Handle, windows/IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle
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
 - IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle
 - windows.devices.alljoyn.interop/IWindowsDevicesAllJoynBusAttachmentFactoryInterop::CreateFromWin32Handle
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
 - IWindowsDevicesAllJoynBusAttachmentFactoryInterop.CreateFromWin32Handle
 - IInspectable .CreateFromWin32Handle
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

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable </a>



<a href="/previous-versions/windows/desktop/api/windows.devices.alljoyn.interop/nn-windows-devices-alljoyn-interop-iwindowsdevicesalljoynbusattachmentfactoryinterop">IWindowsDevicesAllJoynBusAttachmentFactoryInterop</a>