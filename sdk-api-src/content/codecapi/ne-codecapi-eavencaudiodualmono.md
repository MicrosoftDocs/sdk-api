---
UID: NE:codecapi.eAVEncAudioDualMono
title: eAVEncAudioDualMono
author: windows-sdk-content
description: Specifies whether 2-channel audio is encoded as stereo or dual mono. This enumeration is used with the AVEncAudioDualMono property.
old-location: dshow\eavencaudiodualmono.htm
old-project: DirectShow
ms.assetid: 5204ca69-947a-4099-a571-b2c0047d9f7f
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: codecapi/eAVEncAudioDualMono, codecapi/eAVEncAudioDualMono_Off, codecapi/eAVEncAudioDualMono_On, codecapi/eAVEncAudioDualMono_SameAsInput, dshow.eavencaudiodualmono, eAVEncAudioDualMono, eAVEncAudioDualMono enumeration [DirectShow], eAVEncAudioDualMonoEnumeration, eAVEncAudioDualMono_Off, eAVEncAudioDualMono_On, eAVEncAudioDualMono_SameAsInput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncAudioDualMono
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVEncAudioDualMono enumeration


## -description



Specifies whether 2-channel audio is encoded as stereo or dual mono. This enumeration is used with the <a href="https://msdn.microsoft.com/37f25590-69c2-43bd-a5d4-2262457cb39d">AVEncAudioDualMono</a> property.




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




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

