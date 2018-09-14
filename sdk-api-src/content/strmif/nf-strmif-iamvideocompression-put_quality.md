---
UID: NF:strmif.IAMVideoCompression.put_Quality
title: IAMVideoCompression::put_Quality
author: windows-sdk-content
description: The put_Quality method sets the compression quality.
old-location: dshow\iamvideocompression_put_quality.htm
tech.root: DirectShow
ms.assetid: 7ecc00f9-73d4-4d26-b7b0-1b6419027d69
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMVideoCompression interface [DirectShow],put_Quality method, IAMVideoCompression.put_Quality, IAMVideoCompression::put_Quality, IAMVideoCompressionput_Quality, dshow.iamvideocompression_put_quality, put_Quality, put_Quality method [DirectShow], put_Quality method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::put_Quality
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoCompression.put_Quality
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoCompression::put_Quality


## -description



The <code>put_Quality</code> method sets the compression quality.




## -parameters




### -param Quality [in]

Specifies the quality as a value between 0.0 and 1.0, where 1.0 indicates the best quality and 0.0 indicates the worst quality. If the value is negative, the filter will use the default quality.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



To determine if the filter supports this method, call the <a href="https://msdn.microsoft.com/d8ba2ba2-510a-4fb8-844e-48059ec4ef0d">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanQuality</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default quality.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>



<a href="https://msdn.microsoft.com/a34b6d15-3c84-476e-bd2f-ee10b59ded82">IAMVideoCompression::get_Quality</a>
 

 

