---
UID: NF:windows.devices.display.core.interop.IDisplayPathInterop.CreateSourcePresentationHandle
title: IDisplayPathInterop::CreateSourcePresentationHandle
description: Creates an NT handle for controlling access to scanout on this path.
helpviewer_keywords: ["IDisplayPathInterop::CreateSourcePresentationHandle"]
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
 - IDisplayPathInterop::CreateSourcePresentationHandle
f1_keywords:
 - IDisplayPathInterop::CreateSourcePresentationHandle
 - windows.devices.display.core.interop/IDisplayPathInterop::CreateSourcePresentationHandle
---

## -description

Creates an NT handle for controlling access to scanout on this path. A compositor application can choose to broker access to paths that it controls using these objects. Your application can call [IDisplayDeviceInterop.OpenSharedHandle](nf-windows-devices-display-core-interop-idisplaydeviceinterop-opensharedhandle.md) to create a [DisplaySource](/uwp/api/windows.devices.display.core.displaysource) object from this handle.

## -parameters

### -param pValue

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)\***

A pointer to a **HANDLE** that receives the newly created source presentation object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

This method returns **S_OK** if it succeeded, otherwise a failure code indicating why it failed. If it succeeded, then *pValue* will always point to the newly created handle.

## -remarks

Multiple processes can have handles of the same object, enabling use of the object for interprocess synchronization or sharing. These object-sharing mechanisms are available.

* A process can specify the object handle in a call to the [DuplicateHandle](../handleapi/nf-handleapi-duplicatehandle.md) function to create a duplicate handle that can be used by another process.
* A process can specify the name of the object in a call to the [IDisplayDeviceInterop.OpenSharedHandle](nf-windows-devices-display-core-interop-idisplaydeviceinterop-opensharedhandle.md) function.

Use the [CloseHandle](../handleapi/nf-handleapi-closehandle.md) function to close the handle. The system closes the handle automatically when the process terminates. The object is destroyed when its last handle has been closed and its last interface reference has been released.

## -see-also
