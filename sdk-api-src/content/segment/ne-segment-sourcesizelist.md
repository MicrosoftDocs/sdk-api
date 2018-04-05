---
UID: NE:segment.SourceSizeList
title: SourceSizeList
author: windows-driver-content
description: This topic applies to Windows XP or later.
old-location: mstv\sourcesizelist.htm
old-project: mstv
ms.assetid: 579c4993-6238-47c7-b61c-398568c1fb94
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: MSVidCtlSourceSizeListEnumeration, SourceSizeList, SourceSizeList enumeration [Microsoft TV Technologies], enumeration [Microsoft TV Technologies], mstv.sourcesizelist, segment/SourceSizeList, segment/sslClipByClipRect, segment/sslClipByOverScan, segment/sslFullSize, sslClipByClipRect, sslClipByOverScan, sslFullSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: segment.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	segment.h
api_name:
-	SourceSizeList
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# SourceSizeList enumeration


## -description



This topic applies to Windows XP or later.
        



The <b>SourceSizeList</b> enumeration is used to indicate how the VMR will clip the source video rectangle.


## -enum-fields




### -field sslFullSize

Do not clip the source video rectangle.


### -field sslClipByOverScan

Clip the source video rectangle by the value specified in the last call to <a href="https://msdn.microsoft.com/141df99b-4fc7-439c-953e-1fa1c544258e">IMSVidVideoRenderer::put_OverScan</a>.


### -field sslClipByClipRect

Clip the source video rectangle by the value specified in the last call to <a href="https://msdn.microsoft.com/c72d8134-ff6c-46b4-b567-35638aef53cd">IMSVidVideoRenderer::put_ClippedSourceRect</a>



## -see-also




<a href="https://msdn.microsoft.com/312a2c1e-5332-4a2d-ada9-1dc8236f4170">IMSVidVideoRenderer::get_SourceSize</a>



<a href="https://msdn.microsoft.com/c792f064-a137-4872-8c79-6e924b6023f0">IMSVidVideoRenderer::put_SourceSize</a>



<a href="https://msdn.microsoft.com/3c21f2c6-8eff-4fe5-a383-057f3394d9ee">Video Control Enumerations</a>
 

 

