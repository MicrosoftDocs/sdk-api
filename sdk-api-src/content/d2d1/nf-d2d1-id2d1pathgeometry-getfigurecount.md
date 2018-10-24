---
UID: NF:d2d1.ID2D1PathGeometry.GetFigureCount
title: ID2D1PathGeometry::GetFigureCount
author: windows-sdk-content
description: Retrieves the number of figures in the path geometry.
old-location: direct2d\ID2D1PathGeometry_GetFigureCount.htm
tech.root: Direct2D
ms.assetid: f46d28f6-5f46-45eb-85c9-6d3b21fa2cff
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetFigureCount, GetFigureCount method [Direct2D], GetFigureCount method [Direct2D],ID2D1PathGeometry interface, ID2D1PathGeometry interface [Direct2D],GetFigureCount method, ID2D1PathGeometry.GetFigureCount, ID2D1PathGeometry::GetFigureCount, d2d1/ID2D1PathGeometry::GetFigureCount, direct2d.ID2D1PathGeometry_GetFigureCount
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
 - ID2D1PathGeometry.GetFigureCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1PathGeometry::GetFigureCount


## -description


Retrieves the number of figures in the path geometry.


## -parameters




### -param count [out]

Type: <b>UINT32*</b>

A pointer that receives the number of figures in the path geometry when this method returns. You must allocate storage for this parameter.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>
 

 

