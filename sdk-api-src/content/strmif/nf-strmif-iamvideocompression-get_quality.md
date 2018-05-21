---
UID: NF:strmif.IAMVideoCompression.get_Quality
title: IAMVideoCompression::get_Quality
author: windows-driver-content
description: The get_Quality method retrieves the current compression quality.
old-location: dshow\iamvideocompression_get_quality.htm
old-project: DirectShow
ms.assetid: a34b6d15-3c84-476e-bd2f-ee10b59ded82
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMVideoCompression interface [DirectShow],get_Quality method, IAMVideoCompression.get_Quality, IAMVideoCompression::get_Quality, IAMVideoCompressionget_Quality, dshow.iamvideocompression_get_quality, get_Quality, get_Quality method [DirectShow], get_Quality method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::get_Quality
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMVideoCompression.get_Quality
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoCompression::get_Quality


## -description



The <code>get_Quality</code> method retrieves the current compression quality.




## -parameters




### -param pQuality [out]

Pointer to a variable that receives the relative compression quality. The quality is expressed as a value between 0.0 and 1.0, where 1.0 indicates the best quality and 0.0 indicates the worst quality. If the value is negative, the filter will use the default quality.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The exact meaning of the quality setting depends on the filter.

To determine if the filter supports this method, call the <a href="https://msdn.microsoft.com/d8ba2ba2-510a-4fb8-844e-48059ec4ef0d">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanQuality</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default quality.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>



<a href="https://msdn.microsoft.com/7ecc00f9-73d4-4d26-b7b0-1b6419027d69">IAMVideoCompression::put_Quality</a>
 

 

