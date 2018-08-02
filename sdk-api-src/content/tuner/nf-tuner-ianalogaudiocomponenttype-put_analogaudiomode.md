---
UID: NF:tuner.IAnalogAudioComponentType.put_AnalogAudioMode
title: IAnalogAudioComponentType::put_AnalogAudioMode
author: windows-sdk-content
description: The put_AnalogAudioMode method specifies the analog audio mode.
old-location: mstv\ianalogaudiocomponenttype_put_analogaudiomode.htm
old-project: mstv
ms.assetid: cb3c4db6-8364-4c95-82d5-62276f26c7bb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAnalogAudioComponentType interface [Microsoft TV Technologies],put_AnalogAudioMode method, IAnalogAudioComponentType.put_AnalogAudioMode, IAnalogAudioComponentType::put_AnalogAudioMode, IAnalogAudioComponentTypeput_AnalogAudioMode, mstv.ianalogaudiocomponenttype_put_analogaudiomode, put_AnalogAudioMode, put_AnalogAudioMode method [Microsoft TV Technologies], put_AnalogAudioMode method [Microsoft TV Technologies],IAnalogAudioComponentType interface, tuner/IAnalogAudioComponentType::put_AnalogAudioMode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IAnalogAudioComponentType.put_AnalogAudioMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnalogAudioComponentType::put_AnalogAudioMode


## -description



The <b>put_AnalogAudioMode</b> method specifies the analog audio mode.




## -parameters




### -param Mode [in]

Specifies the analog audio mode. This parameter is a variable of type <a href="https://msdn.microsoft.com/70e26550-0a8f-484e-b919-cfefdcf95f6b">TVAudioMode</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/bd2256b4-6e9a-4520-8988-d271fb2b84af">IAnalogAudioComponentType Interface</a>



<a href="https://msdn.microsoft.com/63c5f2a0-5524-4df0-bc0d-fcd7c6b36167">get_AnalogAudioMode</a>
 

 

