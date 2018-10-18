---
UID: NF:d2d1_1.ID2D1Device.CreateDeviceContext
title: ID2D1Device::CreateDeviceContext
author: windows-sdk-content
description: Creates a new device context from a Direct2D device.
old-location: direct2d\id2d1device_createdevicecontext.htm
tech.root: direct2d
ms.assetid: d14255d4-ae59-42b4-ada9-bd7a3c5e8024
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CreateDeviceContext, CreateDeviceContext method [Direct2D], CreateDeviceContext method [Direct2D],ID2D1Device interface, ID2D1Device interface [Direct2D],CreateDeviceContext method, ID2D1Device.CreateDeviceContext, ID2D1Device::CreateDeviceContext, d2d1_1/ID2D1Device::CreateDeviceContext, direct2d.id2d1device_createdevicecontext
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
req.lib: D2d1.lib
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
 - ID2D1Device.CreateDeviceContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device::CreateDeviceContext


## -description


Creates a new device context from a Direct2D device.


## -parameters




### -param options

Type: <b><a href="https://msdn.microsoft.com/be4e6eb7-0767-4faf-9f27-eeb3bed48244">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The options to be applied to the created device context.


### -param deviceContext [out]

Type: <b>const <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>**</b>

When this method returns, contains the address of a pointer to the new device context.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The new device context will not have a  selected target bitmap. The caller must create and select a bitmap as the target surface of the context.




## -see-also




<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>



<a href="https://msdn.microsoft.com/66914048-7bef-4551-bb14-5ab67c727dc5">ID2D1DeviceContext::SetTarget</a>
 

 

