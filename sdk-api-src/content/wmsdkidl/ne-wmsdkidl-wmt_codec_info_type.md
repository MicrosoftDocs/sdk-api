---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# WMT_CODEC_INFO_TYPE enumeration


## -description



The <b>WMT_CODEC_INFO_TYPE</b> enumeration type defines the broad categories of codecs supported by this SDK.




## -enum-fields




### -field WMT_CODECINFO_AUDIO

Audio codec.


### -field WMT_CODECINFO_VIDEO

Video codec.


### -field WMT_CODECINFO_UNKNOWN

Codec of an unknown type.


## -remarks



This type is used when adding or retrieving the codecs used in a file using <a href="https://msdn.microsoft.com/685eaf9e-6cc8-4c38-be34-afa4b504a326">IWMHeaderInfo2::GetCodecInfo</a> and <a href="https://msdn.microsoft.com/4c5bc019-e4bb-419b-91ce-779fd36d7b4c">IWMHeaderInfo3::AddCodecInfo</a>. When enumerating codecs with the methods of <b>IWMCodecInfo</b>, <b>IWMCodecInfo2</b>, and <b>IWMCodecInfo3</b>, you do not use this type. Those methods use the major media type GUIDs instead.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

