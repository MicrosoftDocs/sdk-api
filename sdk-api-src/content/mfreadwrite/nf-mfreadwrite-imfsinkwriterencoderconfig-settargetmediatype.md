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

# IMFSinkWriterEncoderConfig::SetTargetMediaType


## -description


Dynamically changes the target media type that Sink Writer is encoding to. 


## -parameters




### -param dwStreamIndex [in]

Specifies the stream index.


### -param pTargetMediaType [in]

The new media format to encode to.


### -param pEncodingParameters [in]

The new set of encoding parameters to configure the encoder with.
    If not specified, previously provided parameters will be used.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The new media type must be supported by the media sink being used and by     the encoder MFTs installed on the system.





## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/3a0d090d-9eb1-4624-989b-c5da27b988aa">IMFSinkWriterEncoderConfig</a>



<a href="https://msdn.microsoft.com/77E6CB22-E3B5-4D5E-8876-48582F75AA5C">IMFSinkWriterEx</a>
 

 

