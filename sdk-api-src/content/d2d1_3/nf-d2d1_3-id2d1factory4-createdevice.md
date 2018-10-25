---
UID: NF:d2d1_3.ID2D1Factory4.CreateDevice
title: ID2D1Factory4::CreateDevice
author: windows-sdk-content
description: Creates an ID2D1Device3 object.
old-location: direct2d\id2d1factory4_createdevice.htm
tech.root: direct2d
ms.assetid: CF34DB7E-39CC-4044-9DF4-838EC19C1B04
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory4 interface, ID2D1Factory4 interface [Direct2D],CreateDevice method, ID2D1Factory4.CreateDevice, ID2D1Factory4::CreateDevice, d2d1_3/ID2D1Factory4::CreateDevice, direct2d.id2d1factory4_createdevice
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
 - ID2D1Factory4.CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory4::CreateDevice


## -description


Creates an <a href="https://msdn.microsoft.com/60CB6308-85BE-424B-9950-1C8617D08A09">ID2D1Device3</a> object.


## -parameters




### -param dxgiDevice [in]

Type: <b><a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a>*</b>

The IDXGIDevice object used when creating the <a href="https://msdn.microsoft.com/60CB6308-85BE-424B-9950-1C8617D08A09">ID2D1Device3</a>.


### -param d2dDevice3 [out]

Type: <b><a href="https://msdn.microsoft.com/60CB6308-85BE-424B-9950-1C8617D08A09">ID2D1Device3</a>**</b>

The requested <a href="https://msdn.microsoft.com/60CB6308-85BE-424B-9950-1C8617D08A09">ID2D1Device3</a> object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7E470D6B-9393-4660-B8B3-28E77495185E">ID2D1Factory4</a>
 

 

