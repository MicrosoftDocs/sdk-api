---
UID: NF:windows.devices.display.core.interop.IDisplayDeviceInterop.OpenSharedHandle
title: IDisplayDeviceInterop::OpenSharedHandle
description: Opens a handle for shared primary surfaces, shared fences, and source presentation handles.
helpviewer_keywords: ["IDisplayDeviceInterop::OpenSharedHandle"]
ms.date: 02/10/2020
tech.root: winrt
req.header: windows.devices.display.core.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: d3d12.lib
req.dll: d3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - IDisplayDeviceInterop::OpenSharedHandle
f1_keywords:
 - IDisplayDeviceInterop::OpenSharedHandle
 - windows.devices.display.core.interop/IDisplayDeviceInterop::OpenSharedHandle
---

## -description

Opens a handle for shared primary surfaces, shared fences, and source presentation handles.

## -parameters

### -param NTHandle

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

An NT handle for a shared primary surface, shared fence, or source presentation handle.

### -param riid

Type: **REFIID**

A reference to the interface identifier (IID) for the default interface of one of the following Windows Runtime classes. An IID is a **[GUID](../guiddef/ns-guiddef-guid.md)**.

* [IDisplaySurface](/uwp/api/windows.devices.display.core.displaysurface)
* [IDisplayFence](/uwp/api/windows.devices.display.core.displayfence)
* [IDisplaySource](/uwp/api/windows.devices.display.core.displaysource)

### -param ppvObj

Type: **void\*\***

A pointer to a memory block that receives a pointer to the interface specified by the *riid* argument.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

Returns **S_OK** on success, or a failure code describing the problem on failure.

## -remarks

You can use this method to open any shared fence, but you can open a surface only if it was created as primary. Primary surfaces are surfaces intended to be used directly by the display hardware to scan out. Most typical Direct3D surfaces are not created as primaries unless they were created for use in a swap-chain back buffer. [DisplayDevice.CreatePrimary](/uwp/api/windows.devices.display.core.displaydevice.createprimary) always creates a surface as a primary, since it is always intended to be used to scan out.

Opening a source presentation handle is similar to calling [CreateScanoutSource](/uwp/api/windows.devices.display.core.displaydevice.createscanoutsource) for the target of the presentation handle, except that it isn't necessary to have created the [DisplayDevice](/uwp/api/windows.devices.display.core.displaydevice) from the same [DisplayManager](/uwp/api/windows.devices.display.core.displaymanager) that created the handle. This allows fine-grained access control of scanout.

## -see-also

* [CreateSharedHandle](nf-windows-devices-display-core-interop-idisplaydeviceinterop-createsharedhandle.md)
