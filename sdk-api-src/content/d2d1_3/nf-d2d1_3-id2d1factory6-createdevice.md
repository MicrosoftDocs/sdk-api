---
UID: NF:d2d1_3.ID2D1Factory6.CreateDevice
title: ID2D1Factory6::CreateDevice
author: windows-sdk-content
description: Creates a new Direct2D device from the given IDXGIDevice.
old-location: direct2d\id2d1factory6_createdevice.htm
tech.root: Direct2D
ms.assetid: 980F35D2-7BAB-4F6B-B75B-9582A3CCCAEB
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory6 interface, ID2D1Factory6 interface [Direct2D],CreateDevice method, ID2D1Factory6.CreateDevice, ID2D1Factory6::CreateDevice, d2d1_3/ID2D1Factory6::CreateDevice, direct2d.id2d1factory6_createdevice
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
 - ID2D1Factory6.CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory6::CreateDevice


## -description


Creates a new Direct2D device from the given IDXGIDevice.


## -parameters




### -param dxgiDevice [in]

Type: <b>IDXGIDevice*</b>

The IDXGIDevice to create the Direct2D device from.


### -param d2dDevice5 [out]

Type: <b>ID2D1Device5**</b>

The created device.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/79656026-7197-4EF4-A8DD-7E65D43D1F18">ID2D1Factory6</a>
 

 

