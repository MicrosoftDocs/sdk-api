---
UID: NF:d2d1_3.ID2D1Device2.CreateDeviceContext
title: ID2D1Device2::CreateDeviceContext
author: windows-sdk-content
description: Creates a new ID2D1DeviceContext2 from a Direct2D device.
old-location: direct2d\id2d1device2_createdevicecontext.htm
tech.root: Direct2D
ms.assetid: 92BC91A0-CD67-4F7B-9B8A-1301DD14C35C
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CreateDeviceContext, CreateDeviceContext method [Direct2D], CreateDeviceContext method [Direct2D],ID2D1Device2 interface, ID2D1Device2 interface [Direct2D],CreateDeviceContext method, ID2D1Device2.CreateDeviceContext, ID2D1Device2::CreateDeviceContext, d2d1_3/ID2D1Device2::CreateDeviceContext, direct2d.id2d1device2_createdevicecontext
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
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Device2.CreateDeviceContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device2::CreateDeviceContext


## -description


Creates a new <a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a> from a Direct2D device.


## -parameters




### -param options

Type: <b><a href="https://msdn.microsoft.com/be4e6eb7-0767-4faf-9f27-eeb3bed48244">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The options to be applied to the created device context.


### -param deviceContext2 [out]

Type: <b><a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>**</b>

When this method returns, contains the address of a pointer to the new device context.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1B34AEFD-BBA7-4759-B80A-89D9BFC1933D">ID2D1Device2</a>
 

 

