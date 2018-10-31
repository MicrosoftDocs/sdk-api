---
UID: NF:d2d1effectauthor.ID2D1EffectContext.GetDpi
title: ID2D1EffectContext::GetDpi
author: windows-sdk-content
description: Gets the unit mapping that an effect will use for properties that could be in either dots per inch (dpi) or pixels.
old-location: direct2d\id2d1contextinternal_getdpi.htm
tech.root: direct2d
ms.assetid: 465D75BF-67A0-410C-950E-DB42995379B0
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDpi, GetDpi method [Direct2D], GetDpi method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],GetDpi method, ID2D1EffectContext.GetDpi, ID2D1EffectContext::GetDpi, d2d1effectauthor/ID2D1EffectContext::GetDpi, direct2d.id2d1contextinternal_getdpi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2D1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.GetDpi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1EffectContext::GetDpi


## -description


Gets the unit mapping that an effect will use for properties that could be in either dots per inch (dpi) or pixels.


## -parameters




### -param dpiX [out]

Type: <b>FLOAT*</b>

The dpi on the x-axis.


### -param dpiY [out]

Type: <b>FLOAT*</b>

The dpi on the y-axis.


## -returns



This method does not return a value.




## -remarks



 If the <a href="https://msdn.microsoft.com/1ba11761-f3e9-4996-8494-384db5bddc99">D2D1_UNIT_MODE</a> is <b>D2D1_UNIT_MODE_PIXELS</b>, both <i>dpiX</i> and <i>dpiY</i> will be set to 96.




## -see-also




<a href="https://msdn.microsoft.com/6BE6DF90-C5B7-4377-9DBF-804AB1C91FEE">ID2D1EffectContext</a>



<a href="https://msdn.microsoft.com/0EBA4FDB-A9EA-4FCF-BF40-3D73ED356CD4">ID2D1EffectImpl::PrepareForRender</a>
 

 

