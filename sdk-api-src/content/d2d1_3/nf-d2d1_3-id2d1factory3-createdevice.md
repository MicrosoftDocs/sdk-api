---
UID: NF:d2d1_3.ID2D1Factory3.CreateDevice
title: ID2D1Factory3::CreateDevice
author: windows-sdk-content
description: Creates an ID2D1Device2 object.
old-location: direct2d\id2d1factory3_createdevice.htm
tech.root: Direct2D
ms.assetid: 17AE8381-2CAA-4607-B63D-17F76DF0D814
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory3 interface, ID2D1Factory3 interface [Direct2D],CreateDevice method, ID2D1Factory3.CreateDevice, ID2D1Factory3::CreateDevice, d2d1_3/ID2D1Factory3::CreateDevice, direct2d.id2d1factory3_createdevice
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
 - ID2D1Factory3.CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory3::CreateDevice


## -description


Creates an <a href="https://msdn.microsoft.com/1B34AEFD-BBA7-4759-B80A-89D9BFC1933D">ID2D1Device2</a> object. 


## -parameters




### -param dxgiDevice [in]

Type: <b><a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a>*</b>

The <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> object used when creating  the <a href="https://msdn.microsoft.com/1B34AEFD-BBA7-4759-B80A-89D9BFC1933D">ID2D1Device2</a>.


### -param d2dDevice2 [out]

Type: <b><a href="https://msdn.microsoft.com/1B34AEFD-BBA7-4759-B80A-89D9BFC1933D">ID2D1Device2</a>**</b>

The requested <a href="https://msdn.microsoft.com/1B34AEFD-BBA7-4759-B80A-89D9BFC1933D">ID2D1Device2</a> object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/95923BAA-0A26-45BF-85F7-8994B70B7D92">ID2D1Factory3</a>
 

 

