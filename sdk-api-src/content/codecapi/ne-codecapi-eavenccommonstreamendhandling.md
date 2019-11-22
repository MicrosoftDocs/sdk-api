---
UID: NE:codecapi.eAVEncCommonStreamEndHandling
title: eAVEncCommonStreamEndHandling (codecapi.h)

description: Specifies whether the encoder discards partial groups of pictures (GOPs) at the end of the stream. This enumeration is used with the AVEncCommonStreamEndHandling codec property.
old-location: dshow\eavenccommonstreamendhandling.htm
tech.root: DirectShow
ms.assetid: 406dbfe6-d5c8-44b1-9052-88df40a6a522

ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncCommonStreamEndHandling, codecapi/eAVEncCommonStreamEndHandling_DiscardPartial, codecapi/eAVEncCommonStreamEndHandling_EnsureComplete, dshow.eavenccommonstreamendhandling, eAVEncCommonStreamEndHandling, eAVEncCommonStreamEndHandling enumeration [DirectShow], eAVEncCommonStreamEndHandlingEnumeration, eAVEncCommonStreamEndHandling_DiscardPartial, eAVEncCommonStreamEndHandling_EnsureComplete
ms.topic: enum
f1_keywords: 
 - "codecapi/eAVEncCommonStreamEndHandling"
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
 - eAVEncCommonStreamEndHandling
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncCommonStreamEndHandling enumeration


## -description



Specifies whether the encoder discards partial groups of pictures (GOPs) at the end of the stream. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avenccommonstreamendhandling-property">AVEncCommonStreamEndHandling</a> codec property.




## -enum-fields




### -field eAVEncCommonStreamEndHandling_DiscardPartial

If there is a partial GOP at the end of the stream, the encoder will discard it.


### -field eAVEncCommonStreamEndHandling_EnsureComplete

If there is a partial GOP at the end of the stream, the encoder will adjust the GOP and encode all of the stream data.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 

