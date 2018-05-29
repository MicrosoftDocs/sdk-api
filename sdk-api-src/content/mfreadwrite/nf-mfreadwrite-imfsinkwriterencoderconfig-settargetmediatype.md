---
UID: NF:mfreadwrite.IMFSinkWriterEncoderConfig.SetTargetMediaType
title: IMFSinkWriterEncoderConfig::SetTargetMediaType
author: windows-sdk-content
description: Dynamically changes the target media type that Sink Writer is encoding to.
old-location: mf\imfsinkwriterencoderconfig_settargetmediatype.htm
old-project: medfound
ms.assetid: 26d6ee83-5899-40e7-8b71-ca47f5b0d1c1
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFSinkWriterEncoderConfig interface [Media Foundation],SetTargetMediaType method, IMFSinkWriterEncoderConfig.SetTargetMediaType, IMFSinkWriterEncoderConfig::SetTargetMediaType, SetTargetMediaType, SetTargetMediaType method [Media Foundation], SetTargetMediaType method [Media Foundation],IMFSinkWriterEncoderConfig interface, mf.imfsinkwriterencoderconfig_settargetmediatype, mfreadwrite/IMFSinkWriterEncoderConfig::SetTargetMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfreadwrite.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfreadwrite.h
api_name:
-	IMFSinkWriterEncoderConfig.SetTargetMediaType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

