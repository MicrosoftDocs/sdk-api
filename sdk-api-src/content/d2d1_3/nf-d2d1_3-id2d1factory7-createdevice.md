---
UID: NF:d2d1_3.ID2D1Factory7.CreateDevice
title: ID2D1Factory7::CreateDevice (d2d1_3.h)
author: windows-sdk-content
description: Creates a new Direct2D device from the given IDXGIDevice.
old-location: direct2d\id2d1factory7_createdevice.htm
tech.root: Direct2D
ms.assetid: 6E40B8EA-AF61-40CF-B085-13954EDFA71F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory7 interface, ID2D1Factory7 interface [Direct2D],CreateDevice method, ID2D1Factory7.CreateDevice, ID2D1Factory7::CreateDevice, d2d1_3/ID2D1Factory7::CreateDevice, direct2d.id2d1factory7_createdevice
ms.topic: method
f1_keywords: 
 - "d2d1_3/ID2D1Factory7.CreateDevice"
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
 - ID2D1Factory7.CreateDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory7::CreateDevice


## -description


Creates a new Direct2D device from the given IDXGIDevice


## -parameters




### -param dxgiDevice [in]

Type: <b>IDXGIDevice*</b>

The IDXGIDevice from which to create the Direct2D device.


### -param d2dDevice6 [out]

Type: <b>ID2D1Device6**</b>

The created device.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1factory7">ID2D1Factory7</a>
 

 

