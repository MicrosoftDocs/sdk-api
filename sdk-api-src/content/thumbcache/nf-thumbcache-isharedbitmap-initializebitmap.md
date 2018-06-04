---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ISharedBitmap::InitializeBitmap


## -description


Initializes a new <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object with a given bitmap.


## -parameters




### -param hbm [in]

Type: <b>HBITMAP</b>

A handle to the bitmap with which to initialize a new <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object. The bitmap must be a DIB.


### -param wtsAT [in]

Type: <b>WTS_ALPHATYPE</b>

The alpha type of the bitmap image.  May be one of the following values.



#### WTSAT_UNKNOWN

Cannot determine whether the bitmap has an alpha channel.



#### WTSAT_RGB

The bitmap does not contain an alpha channel for transparency.



#### WTSAT_ARGB

The bitmap contains an alpha channel for transparency.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When an <a href="https://msdn.microsoft.com/72be7757-f969-4f4f-ada1-71789b8d1de0">ISharedBitmap</a> object is instantiated by the client (as opposed to being returned by the <a href="https://msdn.microsoft.com/3b5069e2-f20b-4c43-a9e7-334366980f5c">IThumbnailCache::GetThumbnailByID</a> or <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> methods), the underlying bitmap will not reside in shared memory.



