---
UID: NF:tuner.IAnalogAudioComponentType.put_AnalogAudioMode
title: IAnalogAudioComponentType::put_AnalogAudioMode (tuner.h)
description: The put_AnalogAudioMode method specifies the analog audio mode.helpviewer_keywords: ["IAnalogAudioComponentType interface [Microsoft TV Technologies]","put_AnalogAudioMode method","IAnalogAudioComponentType.put_AnalogAudioMode","IAnalogAudioComponentType::put_AnalogAudioMode","IAnalogAudioComponentTypeput_AnalogAudioMode","mstv.ianalogaudiocomponenttype_put_analogaudiomode","put_AnalogAudioMode","put_AnalogAudioMode method [Microsoft TV Technologies]","put_AnalogAudioMode method [Microsoft TV Technologies]","IAnalogAudioComponentType interface","tuner/IAnalogAudioComponentType::put_AnalogAudioMode"]
old-location: mstv\ianalogaudiocomponenttype_put_analogaudiomode.htm
tech.root: mstv
ms.assetid: cb3c4db6-8364-4c95-82d5-62276f26c7bb
ms.date: 12/05/2018
ms.keywords: IAnalogAudioComponentType interface [Microsoft TV Technologies],put_AnalogAudioMode method, IAnalogAudioComponentType.put_AnalogAudioMode, IAnalogAudioComponentType::put_AnalogAudioMode, IAnalogAudioComponentTypeput_AnalogAudioMode, mstv.ianalogaudiocomponenttype_put_analogaudiomode, put_AnalogAudioMode, put_AnalogAudioMode method [Microsoft TV Technologies], put_AnalogAudioMode method [Microsoft TV Technologies],IAnalogAudioComponentType interface, tuner/IAnalogAudioComponentType::put_AnalogAudioMode
f1_keywords:
- tuner/IAnalogAudioComponentType.put_AnalogAudioMode
dev_langs:
- c++
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
- IAnalogAudioComponentType.put_AnalogAudioMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAnalogAudioComponentType::put_AnalogAudioMode


## -description



The <b>put_AnalogAudioMode</b> method specifies the analog audio mode.




## -parameters




### -param Mode [in]

Specifies the analog audio mode. This parameter is a variable of type <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-tvaudiomode">TVAudioMode</a>.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogaudiocomponenttype">IAnalogAudioComponentType Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogaudiocomponenttype-get_analogaudiomode">get_AnalogAudioMode</a>
 

 

