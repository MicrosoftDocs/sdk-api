---
UID: NF:d2d1_3.ID2D1Ink.SetSegments
title: ID2D1Ink::SetSegments
author: windows-sdk-content
description: Updates the specified segments in this ink object with new control points.
old-location: direct2d\id2d1ink_setsegments.htm
tech.root: direct2d
ms.assetid: 930D9772-D922-4CEB-A97C-06F263543D81
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID2D1Ink interface [Direct2D],SetSegments method, ID2D1Ink.SetSegments, ID2D1Ink::SetSegments, SetSegments, SetSegments method [Direct2D], SetSegments method [Direct2D],ID2D1Ink interface, d2d1_3/ID2D1Ink::SetSegments, direct2d.id2d1ink_setsegments
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
 - ID2D1Ink.SetSegments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Ink::SetSegments


## -description


Updates the specified segments in this ink object with new control points.


## -parameters




### -param startSegment

Type: <b>UINT32</b>

The index of the first segment in this ink object to update.


### -param segments [in]

Type: <b>const <a href="https://msdn.microsoft.com/27F1F78B-2478-4F5D-BF56-9931E767C358">D2D1_INK_BEZIER_SEGMENT</a>*</b>

A pointer to the array of segment data to be used in the update.


### -param segmentsCount

Type: <b>UINT32</b>

The number of segments in this ink object that will be updated with new data. Note that segmentsCount must be less than or equal to the number of segments in the ink object minus startSegment.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a>
 

 

