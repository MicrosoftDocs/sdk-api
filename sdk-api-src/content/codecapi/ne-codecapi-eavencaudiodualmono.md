---
UID: NE:codecapi.eAVEncAudioDualMono
title: eAVEncAudioDualMono (codecapi.h)
description: Specifies whether 2-channel audio is encoded as stereo or dual mono. This enumeration is used with the AVEncAudioDualMono property.
helpviewer_keywords: ["codecapi/eAVEncAudioDualMono","codecapi/eAVEncAudioDualMono_Off","codecapi/eAVEncAudioDualMono_On","codecapi/eAVEncAudioDualMono_SameAsInput","dshow.eavencaudiodualmono","eAVEncAudioDualMono","eAVEncAudioDualMono enumeration [DirectShow]","eAVEncAudioDualMonoEnumeration","eAVEncAudioDualMono_Off","eAVEncAudioDualMono_On","eAVEncAudioDualMono_SameAsInput"]
old-location: dshow\eavencaudiodualmono.htm
tech.root: DirectShow
ms.assetid: 5204ca69-947a-4099-a571-b2c0047d9f7f
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncAudioDualMono, codecapi/eAVEncAudioDualMono_Off, codecapi/eAVEncAudioDualMono_On, codecapi/eAVEncAudioDualMono_SameAsInput, dshow.eavencaudiodualmono, eAVEncAudioDualMono, eAVEncAudioDualMono enumeration [DirectShow], eAVEncAudioDualMonoEnumeration, eAVEncAudioDualMono_Off, eAVEncAudioDualMono_On, eAVEncAudioDualMono_SameAsInput
f1_keywords:
- codecapi/eAVEncAudioDualMono
dev_langs:
- c++
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- HeaderDef
api_location:
- codecapi.h
api_name:
- eAVEncAudioDualMono
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncAudioDualMono enumeration


## -description



Specifies whether 2-channel audio is encoded as stereo or dual mono. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencaudiodualmono-property">AVEncAudioDualMono</a> property.




## -enum-fields




### -field eAVEncAudioDualMono_SameAsInput

Use the setting specified in the input media type.


### -field eAVEncAudioDualMono_Off

Do not use dual mono encoding.


### -field eAVEncAudioDualMono_On

Use dual mono encoding.


## -remarks



In dual mono encoding, each channel is encoded separately. In stereo encoding, both channels are encoded together.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

