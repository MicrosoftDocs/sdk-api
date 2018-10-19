---
UID: NF:d2d1_3.ID2D1Device4.CreateDeviceContext
title: ID2D1Device4::CreateDeviceContext
author: windows-sdk-content
description: Creates a new ID2D1DeviceContext4 from this Direct2D device.
old-location: direct2d\id2d1device4_createdevicecontext.htm
tech.root: direct2d
ms.assetid: 06F097C4-E417-48EA-A480-62E96C4A1CE6
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CreateDeviceContext, CreateDeviceContext method [Direct2D], CreateDeviceContext method [Direct2D],ID2D1Device4 interface, ID2D1Device4 interface [Direct2D],CreateDeviceContext method, ID2D1Device4.CreateDeviceContext, ID2D1Device4::CreateDeviceContext, d2d1_3/ID2D1Device4::CreateDeviceContext, direct2d.id2d1device4_createdevicecontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
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
 - ID2D1Device4.CreateDeviceContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device4::CreateDeviceContext


## -description


Creates a new <a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a> from this Direct2D device.


## -parameters




### -param options

Type: <b><a href="https://msdn.microsoft.com/be4e6eb7-0767-4faf-9f27-eeb3bed48244">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The options to be applied to the created device context.


### -param deviceContext4 [out]

Type: <b><a href="https://msdn.microsoft.com/59E1F73B-BAD9-4826-BF5B-435E760CC546">ID2D1DeviceContext4</a>**</b>

When this method returns, contains a pointer to the new device context.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B91E4E63-5FB5-4470-A3B9-F94008EAE4E9">ID2D1Device4</a>
 

 

