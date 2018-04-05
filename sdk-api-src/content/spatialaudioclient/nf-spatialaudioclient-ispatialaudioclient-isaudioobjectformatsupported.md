---
UID: NF:spatialaudioclient.ISpatialAudioClient.IsAudioObjectFormatSupported
title: ISpatialAudioClient::IsAudioObjectFormatSupported method
author: windows-driver-content
description: Gets a value indicating whether ISpatialAudioObjectRenderStream supports a the specified format.
old-location: coreaudio\ispatialaudioclient_isaudioobjectformatsupported.htm
old-project: CoreAudio
ms.assetid: 47AB0B3B-E8D0-412F-AC9C-F8BC700E7C23
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: ISpatialAudioClient, ISpatialAudioClient interface [Core Audio], IsAudioObjectFormatSupported method, ISpatialAudioClient::IsAudioObjectFormatSupported, IsAudioObjectFormatSupported method [Core Audio], IsAudioObjectFormatSupported method [Core Audio], ISpatialAudioClient interface, IsAudioObjectFormatSupported,ISpatialAudioClient.IsAudioObjectFormatSupported, coreaudio.ispatialaudioclient_isaudioobjectformatsupported, spatialaudioclient/ISpatialAudioClient::IsAudioObjectFormatSupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
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
req.typenames: AudioObjectType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	spatialaudioclient.h
api_name:
-	ISpatialAudioClient.IsAudioObjectFormatSupported
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ISpatialAudioClient::IsAudioObjectFormatSupported method


## -description


Gets a value indicating whether <a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a> supports a the specified format. 


## -parameters




### -param objectFormat [in]

The format for which support is queried.


## -returns



If the specified format is supported, it returns S_OK. If specified format is unsupported, this method returns AUDCLNT_E_UNSUPPORTED_FORMAT.




## -see-also




<a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a>
 

 

