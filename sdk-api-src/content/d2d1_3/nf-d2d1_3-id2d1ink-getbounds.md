---
UID: NF:d2d1_3.ID2D1Ink.GetBounds
title: ID2D1Ink::GetBounds
author: windows-sdk-content
description: Retrieve the bounds of the geometry, with an optional applied transform.
old-location: direct2d\id2d1ink_getbounds.htm
tech.root: direct2d
ms.assetid: 83BA2631-B3EA-4411-A5F7-265C95A00C9F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBounds, GetBounds method [Direct2D], GetBounds method [Direct2D],ID2D1Ink interface, ID2D1Ink interface [Direct2D],GetBounds method, ID2D1Ink.GetBounds, ID2D1Ink::GetBounds, d2d1_3/ID2D1Ink::GetBounds, direct2d.id2d1ink_getbounds
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
 - ID2D1Ink.GetBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Ink::GetBounds


## -description


Retrieve the bounds of the geometry, with an optional applied transform.


## -parameters




### -param inkStyle [in, optional]

Type: <b><a href="https://msdn.microsoft.com/03853FA5-1377-42FB-A4C2-50069DDF6E2D">ID2D1InkStyle</a>*</b>

The ink style to be used in determining the bounds of this ink object.


### -param worldTransform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

The world transform to be used in determining the bounds of this ink object.


### -param bounds [out]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

When this method returns, contains the bounds of this ink object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a>
 

 

