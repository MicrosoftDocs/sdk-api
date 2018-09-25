---
UID: NF:deviceaccess.CreateDeviceAccessInstance
title: CreateDeviceAccessInstance function
author: windows-sdk-content
description: Creates the object that's used to access a device. The instantiated object implements the IDeviceIoControl and ICreateDeviceAccessAsync interfaces.
old-location: deviceaccess\createdeviceaccessinstance.htm
tech.root: deviceaccess
ms.assetid: 082d6297-20ac-4557-8205-0451482a5758
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateDeviceAccessInstance, CreateDeviceAccessInstance function [Device Access Broker API], deviceaccess.createdeviceaccessinstance, deviceaccess/CreateDeviceAccessInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - deviceaccess.dll
api_name:
 - CreateDeviceAccessInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateDeviceAccessInstance function


## -description


Creates the object that's used to access a device. The instantiated object implements  the <a href="https://msdn.microsoft.com/d285e04e-04d0-4c2a-b9f0-72eebebf4f4b">IDeviceIoControl</a> and <a href="https://msdn.microsoft.com/ebc8d694-c933-4d98-95f5-67b0dd733d4d">ICreateDeviceAccessAsync</a> interfaces.

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
 


The most commonly used values are <b>GENERIC_READ</b>, <b>GENERIC_WRITE</b>, or both (<b>GENERIC_READ</b> | <b>GENERIC_WRITE</b>). For more information, see <a href="https://msdn.microsoft.com/e18cede9-9bf7-4866-850b-5d7fa43a5b0f">Generic Access Rights</a>, <a href="https://msdn.microsoft.com/991d7d94-fae7-406f-b2e3-dee811279366">File Security and Access Rights</a>, <a href="https://msdn.microsoft.com/c534e853-b61f-414d-befe-8d3c4bf08d22">File Access Rights Constants</a>, <a href="https://msdn.microsoft.com/094cac29-c66d-409e-8928-878dc693d393">Creating and Opening Files</a>, and <a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a>.
 



### -param createAsync

Asynchronous interface to control binding for this instance.  For more information, see <a href="https://msdn.microsoft.com/ebc8d694-c933-4d98-95f5-67b0dd733d4d">ICreateDeviceAccessAsync</a>.


## -returns



<b>S_OK</b> if the underlying object and asynchronous operation are created successfully; an appropriate error otherwise.  Note that this function doesn't perform the actual binding.That happens as part of the asynchronous operation.



