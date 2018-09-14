---
UID: NF:mfreadwrite.IMFSinkWriterEncoderConfig.PlaceEncodingParameters
title: IMFSinkWriterEncoderConfig::PlaceEncodingParameters
author: windows-sdk-content
description: Dynamically updates the encoder configuration with a collection of new encoder settings.
old-location: mf\imfsinkwriterencoderconfig_placeencodingparameters.htm
tech.root: medfound
ms.assetid: ea09d806-c869-4a62-8f9d-c35db4e406ff
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFSinkWriterEncoderConfig interface [Media Foundation],PlaceEncodingParameters method, IMFSinkWriterEncoderConfig.PlaceEncodingParameters, IMFSinkWriterEncoderConfig::PlaceEncodingParameters, PlaceEncodingParameters, PlaceEncodingParameters method [Media Foundation], PlaceEncodingParameters method [Media Foundation],IMFSinkWriterEncoderConfig interface, mf.imfsinkwriterencoderconfig_placeencodingparameters, mfreadwrite/IMFSinkWriterEncoderConfig::PlaceEncodingParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfreadwrite.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriterEncoderConfig.PlaceEncodingParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSinkWriterEncoderConfig::PlaceEncodingParameters


## -description


Dynamically updates the encoder configuration with a collection of new encoder settings.


## -parameters




### -param dwStreamIndex [in]

Specifies the stream index.


### -param pEncodingParameters [in]

A set of encoding parameters to configure the encoder with.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The encoder will be configured with these settings after all previously queued input media samples have been sent to it through <a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">IMFTransform::ProcessInput</a>.





## -see-also




<a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a>



<a href="https://msdn.microsoft.com/3a0d090d-9eb1-4624-989b-c5da27b988aa">IMFSinkWriterEncoderConfig</a>



<a href="https://msdn.microsoft.com/77E6CB22-E3B5-4D5E-8876-48582F75AA5C">IMFSinkWriterEx</a>
 

 

