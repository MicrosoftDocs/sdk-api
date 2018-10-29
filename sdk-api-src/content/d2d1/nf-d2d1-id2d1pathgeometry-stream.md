---
UID: NF:d2d1.ID2D1PathGeometry.Stream
title: ID2D1PathGeometry::Stream
author: windows-sdk-content
description: Copies the contents of the path geometry to the specified ID2D1GeometrySink.
old-location: direct2d\ID2D1PathGeometry_Stream.htm
tech.root: Direct2D
ms.assetid: e128b4e7-8fde-44f1-a7a3-928aace0fe7f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ID2D1PathGeometry interface [Direct2D],Stream method, ID2D1PathGeometry.Stream, ID2D1PathGeometry::Stream, Stream, Stream method [Direct2D], Stream method [Direct2D],ID2D1PathGeometry interface, d2d1/ID2D1PathGeometry::Stream, direct2d.ID2D1PathGeometry_Stream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ID2D1PathGeometry.Stream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1PathGeometry::Stream


## -description


Copies the contents of the path geometry to the specified <a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>.


## -parameters




### -param geometrySink [in]

Type: <b><a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>*</b>

The sink to which the path geometry's contents are copied. Modifying this sink does not change the contents of this path geometry.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>
 

 

