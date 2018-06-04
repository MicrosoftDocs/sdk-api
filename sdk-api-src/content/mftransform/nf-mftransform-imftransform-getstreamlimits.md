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

# IMFTransform::GetStreamLimits


## -description



          Gets the minimum and maximum number of input and output streams for this Media Foundation transform (MFT).
        


## -parameters




### -param pdwInputMinimum [out]


            Receives the minimum number of input streams.
          


### -param pdwInputMaximum [out]


            Receives the maximum number of input streams. If there is no maximum, receives the value <b>MFT_STREAMS_UNLIMITED</b>.
          


### -param pdwOutputMinimum [out]


            Receives the minimum number of output streams.
          


### -param pdwOutputMaximum [out]


            Receives the maximum number of output streams. If there is no maximum, receives the value <b>MFT_STREAMS_UNLIMITED</b>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        If the MFT has a fixed number of streams, the minimum and maximum values are the same.
      


        It is not recommended to create an MFT that supports zero inputs or zero outputs. An MFT with no inputs or no outputs may not be compatible with the rest of the Media Foundation pipeline. You should create a Media Foundation sink or source for this purpose instead.
      


        When an MFT is first created, it is not guaranteed to have the minimum number of streams. To find the actual number of streams, call <a href="https://msdn.microsoft.com/491f7f44-fcac-4236-ba5c-e5705267c6c2">IMFTransform::GetStreamCount</a>.
      


        This method should not be called with <b>NULL</b> parameters, although in practice some implementations may allow <b>NULL</b> parameters.
      

If <b>MFT_UNIQUE_METHOD_NAMES</b> is defined before including mftransform.h, this method is renamed <b>MFTGetStreamLimits</b>. See <a href="comparison_of_mfts_and_dmos.htm">Creating Hybrid DMO/MFT Objects</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

