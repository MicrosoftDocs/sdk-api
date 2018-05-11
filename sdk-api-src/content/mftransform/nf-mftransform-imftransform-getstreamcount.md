---
UID: NF:mftransform.IMFTransform.GetStreamCount
title: IMFTransform::GetStreamCount
author: windows-driver-content
description: Gets the current number of input and output streams on this Media Foundation transform (MFT).
old-location: mf\imftransform_getstreamcount.htm
old-project: medfound
ms.assetid: 491f7f44-fcac-4236-ba5c-e5705267c6c2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 491f7f44-fcac-4236-ba5c-e5705267c6c2, GetStreamCount, GetStreamCount method [Media Foundation], GetStreamCount method [Media Foundation],IMFTransform interface, IMFTransform interface [Media Foundation],GetStreamCount method, IMFTransform.GetStreamCount, IMFTransform::GetStreamCount, mf.imftransform_getstreamcount, mftransform/IMFTransform::GetStreamCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTransform.GetStreamCount
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTransform::GetStreamCount


## -description



          Gets the current number of input and output streams on this Media Foundation transform (MFT).
        


## -parameters




### -param pcInputStreams [out]


            Receives the number of input streams.
          


### -param pcOutputStreams [out]


            Receives the number of output streams.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The number of streams includes unselected streams—that is, streams with no media type or a <b>NULL</b> media type.


        This method should not be called with <b>NULL</b> parameters, although in practice some implementations may allow <b>NULL</b> parameters.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetStreamCount</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

