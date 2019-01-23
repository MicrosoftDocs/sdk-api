---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateInk(const D2D1_INK_POINT &,ID2D1Ink)
title: ID2D1DeviceContext2::CreateInk(const D2D1_INK_POINT &,ID2D1Ink)
author: windows-sdk-content
description: Creates a new ID2D1Ink object that starts at the given point.
old-location: direct2d\id2d1devicecontext2_createink.htm
tech.root: Direct2D
ms.assetid: 3079f5d4-3b7d-c3dd-86cd-cca40674bf49
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateInk, CreateInk method [Direct2D], CreateInk method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateInk method, ID2D1DeviceContext2.CreateInk, ID2D1DeviceContext2.CreateInk(const D2D1_INK_POINT &,ID2D1Ink), ID2D1DeviceContext2::CreateInk, ID2D1DeviceContext2::CreateInk(const D2D1_INK_POINT &,ID2D1Ink), d2d1_3/ID2D1DeviceContext2::CreateInk, direct2d.id2d1devicecontext2_createink
ms.topic: method
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID2D1DeviceContext2.CreateInk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DeviceContext2::CreateInk(const D2D1_INK_POINT &,ID2D1Ink)


## -description


Creates a new <a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a> object that starts at the given point.


## -parameters




### -param startPoint [ref]

Type: <b>const <a href="https://msdn.microsoft.com/C18E7B04-12B8-4EB9-BAFB-24FBA99210E9">D2D1_INK_POINT</a></b>

The starting point of the first segment of the first stroke in the new ink object.


### -param ink [out]

Type: <b><a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a>**</b>

When this method returns, contains the address of a pointer to a new ink object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a>
 

 

