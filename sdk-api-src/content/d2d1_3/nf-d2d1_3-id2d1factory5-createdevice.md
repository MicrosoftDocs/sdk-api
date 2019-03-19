---
UID: NF:d2d1_3.ID2D1Factory5.CreateDevice
title: ID2D1Factory5::CreateDevice (d2d1_3.h)
author: windows-sdk-content
description: Creates an ID2D1Device4 object.
old-location: direct2d\id2d1factory5_createdevice.htm
tech.root: Direct2D
ms.assetid: BE77F5AD-82B1-4DB4-8BE0-8C066EA09424
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateDevice, CreateDevice method [Direct2D], CreateDevice method [Direct2D],ID2D1Factory5 interface, ID2D1Factory5 interface [Direct2D],CreateDevice method, ID2D1Factory5.CreateDevice, ID2D1Factory5::CreateDevice, d2d1_3/ID2D1Factory5::CreateDevice, direct2d.id2d1factory5_createdevice
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
 - ID2D1Factory5.CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory5::CreateDevice


## -description


Creates an <a href="https://msdn.microsoft.com/B91E4E63-5FB5-4470-A3B9-F94008EAE4E9">ID2D1Device4</a> object.
        


## -parameters




### -param dxgiDevice [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>*</b>

The IDXGIDevice object used when creating the <a href="https://msdn.microsoft.com/B91E4E63-5FB5-4470-A3B9-F94008EAE4E9">ID2D1Device4</a>.


### -param d2dDevice4 [out]

Type: <b><a href="https://msdn.microsoft.com/B91E4E63-5FB5-4470-A3B9-F94008EAE4E9">ID2D1Device4</a>**</b>

The requested <a href="https://msdn.microsoft.com/B91E4E63-5FB5-4470-A3B9-F94008EAE4E9">ID2D1Device4</a> object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/6D6AA1F7-69AF-4B72-8352-DB443059FF34">ID2D1Factory5</a>
 

 

