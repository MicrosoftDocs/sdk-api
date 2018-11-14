---
UID: NF:d2d1_1.ID2D1DeviceContext.GetDevice
title: ID2D1DeviceContext::GetDevice
author: windows-sdk-content
description: Gets the device associated with a device context.
old-location: direct2d\id2d1devicecontext_getdevice.htm
tech.root: direct2d
ms.assetid: 8c8664cb-d6be-41e0-8415-d60dcd46132a
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetDevice, GetDevice method [Direct2D], GetDevice method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],GetDevice method, ID2D1DeviceContext.GetDevice, ID2D1DeviceContext::GetDevice, d2d1_1/ID2D1DeviceContext::GetDevice, direct2d.id2d1devicecontext_getdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DeviceContext.GetDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1_1.h
: 
- ID2D1DeviceContext.GetDevice
: 
---

# ID2D1DeviceContext::GetDevice


## -description


Gets the device associated with a device context.


## -parameters




### -param device [out]

Type: <b><a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>**</b>

When this method returns, contains the address of a pointer to a Direct2D device associated with this device context.


## -returns



This method does not return a value.




## -remarks



The application can retrieve the device even if it is created from an earlier render target code-path. The application must use an <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a> interface and then call <b>GetDevice</b>. Some functionality for controlling all of the resources for a set of device contexts is maintained only on an <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> object.




## -see-also




<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>
 

 

