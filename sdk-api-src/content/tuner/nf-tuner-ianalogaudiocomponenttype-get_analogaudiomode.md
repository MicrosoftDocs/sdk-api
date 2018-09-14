---
UID: NF:tuner.IAnalogAudioComponentType.get_AnalogAudioMode
title: IAnalogAudioComponentType::get_AnalogAudioMode
author: windows-sdk-content
description: The get_AnalogAudioMode method retrieves the analog audio mode.
old-location: mstv\ianalogaudiocomponenttype_get_analogaudiomode.htm
tech.root: MSTV
ms.assetid: 63c5f2a0-5524-4df0-bc0d-fcd7c6b36167
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAnalogAudioComponentType interface [Microsoft TV Technologies],get_AnalogAudioMode method, IAnalogAudioComponentType.get_AnalogAudioMode, IAnalogAudioComponentType::get_AnalogAudioMode, IAnalogAudioComponentTypeget_AnalogAudioMode, get_AnalogAudioMode, get_AnalogAudioMode method [Microsoft TV Technologies], get_AnalogAudioMode method [Microsoft TV Technologies],IAnalogAudioComponentType interface, mstv.ianalogaudiocomponenttype_get_analogaudiomode, tuner/IAnalogAudioComponentType::get_AnalogAudioMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IAnalogAudioComponentType.get_AnalogAudioMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAnalogAudioComponentType::get_AnalogAudioMode


## -description



The <b>get_AnalogAudioMode</b> method retrieves the analog audio mode.




## -parameters




### -param Mode [out]

Pointer to a <a href="https://msdn.microsoft.com/70e26550-0a8f-484e-b919-cfefdcf95f6b">TVAudioMode</a> variable that receives the analog audio mode.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/bd2256b4-6e9a-4520-8988-d271fb2b84af">IAnalogAudioComponentType Interface</a>



<a href="https://msdn.microsoft.com/cb3c4db6-8364-4c95-82d5-62276f26c7bb">put_AnalogAudioMode</a>
 

 

