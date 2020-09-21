---
UID: NF:deviceaccess.CreateDeviceAccessInstance
title: CreateDeviceAccessInstance function (deviceaccess.h)
description: Creates the object that's used to access a device. The instantiated object implements the IDeviceIoControl and ICreateDeviceAccessAsync interfaces.
helpviewer_keywords: ["CreateDeviceAccessInstance","CreateDeviceAccessInstance function [Device Access Broker API]","deviceaccess.createdeviceaccessinstance","deviceaccess/CreateDeviceAccessInstance"]
old-location: deviceaccess\createdeviceaccessinstance.htm
tech.root: deviceaccess
ms.assetid: 082d6297-20ac-4557-8205-0451482a5758
ms.date: 12/05/2018
ms.keywords: CreateDeviceAccessInstance, CreateDeviceAccessInstance function [Device Access Broker API], deviceaccess.createdeviceaccessinstance, deviceaccess/CreateDeviceAccessInstance
req.header: deviceaccess.h
req.include-header: 
req.target-type: Windows
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
req.lib: Deviceaccess.lib
req.dll: Deviceaccess.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateDeviceAccessInstance
 - deviceaccess/CreateDeviceAccessInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - deviceaccess.dll
api_name:
 - CreateDeviceAccessInstance
---

# CreateDeviceAccessInstance function


## -description

Creates the object that's used to access a device. The instantiated object implements  the <a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-ideviceiocontrol">IDeviceIoControl</a> and <a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-icreatedeviceaccessasync">ICreateDeviceAccessAsync</a> interfaces.

Conditions (FYI):

```

 !defined(__deviceaccess_h__) [-AND-]  ((NTDDI_VERSION >= NTDDI_WIN8)) [-AND-]  defined(__cplusplus)
```

Declaration from header. 

```

 HRESULT WINAPI  
CreateDeviceAccessInstance(  
    _In_ LPCWSTR deviceInterfacePath,  
    _In_ DWORD desiredAccess,  
    _Outptr_ ICreateDeviceAccessAsync **createAsync  
    );
```

## -parameters

### -param deviceInterfacePath [in]

A valid device interface path for the device that this instance should bind to.

### -param desiredAccess [in]

The requested level of access to the device, which can be summarized as read, write, both, or neither (zero).
 


The most commonly used values are <b>GENERIC_READ</b>, <b>GENERIC_WRITE</b>, or both (<b>GENERIC_READ</b> | <b>GENERIC_WRITE</b>). For more information, see <a href="/windows/desktop/SecAuthZ/generic-access-rights">Generic Access Rights</a>, <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>, <a href="/windows/desktop/FileIO/file-access-rights-constants">File Access Rights Constants</a>, <a href="/windows/desktop/FileIO/creating-and-opening-files">Creating and Opening Files</a>, and <a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>.

### -param createAsync

Asynchronous interface to control binding for this instance.  For more information, see <a href="/previous-versions/windows/desktop/api/deviceaccess/nn-deviceaccess-icreatedeviceaccessasync">ICreateDeviceAccessAsync</a>.

## -returns

<b>S_OK</b> if the underlying object and asynchronous operation are created successfully; an appropriate error otherwise.  Note that this function doesn't perform the actual binding.That happens as part of the asynchronous operation.