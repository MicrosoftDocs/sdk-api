---
UID: NE:codecapi.eAVEncCommonStreamEndHandling
title: eAVEncCommonStreamEndHandling
author: windows-sdk-content
description: Specifies whether the encoder discards partial groups of pictures (GOPs) at the end of the stream. This enumeration is used with the AVEncCommonStreamEndHandling codec property.
old-location: dshow\eavenccommonstreamendhandling.htm
tech.root: DirectShow
ms.assetid: 406dbfe6-d5c8-44b1-9052-88df40a6a522
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: codecapi/eAVEncCommonStreamEndHandling, codecapi/eAVEncCommonStreamEndHandling_DiscardPartial, codecapi/eAVEncCommonStreamEndHandling_EnsureComplete, dshow.eavenccommonstreamendhandling, eAVEncCommonStreamEndHandling, eAVEncCommonStreamEndHandling enumeration [DirectShow], eAVEncCommonStreamEndHandlingEnumeration, eAVEncCommonStreamEndHandling_DiscardPartial, eAVEncCommonStreamEndHandling_EnsureComplete
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncCommonStreamEndHandling enumeration


## -description



Specifies whether the encoder discards partial groups of pictures (GOPs) at the end of the stream. This enumeration is used with the <a href="https://msdn.microsoft.com/93cf1299-a8ba-4a14-ad4c-09dd931e18fc">AVEncCommonStreamEndHandling</a> codec property.




## -enum-fields




### -field eAVEncCommonStreamEndHandling_DiscardPartial

If there is a partial GOP at the end of the stream, the encoder will discard it.


### -field eAVEncCommonStreamEndHandling_EnsureComplete

If there is a partial GOP at the end of the stream, the encoder will adjust the GOP and encode all of the stream data.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

