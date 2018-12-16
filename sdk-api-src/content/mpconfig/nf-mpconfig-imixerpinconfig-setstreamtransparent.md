---
UID: NF:mpconfig.IMixerPinConfig.SetStreamTransparent
title: IMixerPinConfig::SetStreamTransparent
author: windows-sdk-content
description: The SetStreamTransparent method sets the stream to transparent.
old-location: dshow\imixerpinconfig_setstreamtransparent.htm
tech.root: DirectShow
ms.assetid: d1f60a35-ffef-4ebb-b331-558772310bcb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetStreamTransparent method, IMixerPinConfig.SetStreamTransparent, IMixerPinConfig::SetStreamTransparent, IMixerPinConfigSetStreamTransparent, SetStreamTransparent, SetStreamTransparent method [DirectShow], SetStreamTransparent method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setstreamtransparent, mpconfig/IMixerPinConfig::SetStreamTransparent
ms.topic: method
req.header: mpconfig.h
req.include-header: 
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
 - IMixerPinConfig.SetStreamTransparent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMixerPinConfig::SetStreamTransparent


## -description



The <code>SetStreamTransparent</code> method sets the stream to transparent.




## -parameters




### -param bStreamTransparent [in]

Value specifying the transparency of the stream. Pass in <b>TRUE</b> to indicate stream is transparent; <b>FALSE</b> to indicate not a transparent stream.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/adee4565-ccc3-4a72-a4ee-c27980868dfa">IMixerPinConfig::GetStreamTransparent</a>
 

 

