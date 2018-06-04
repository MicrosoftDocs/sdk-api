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

# IMFMediaEngineExtension::CanPlayType


## -description


Queries whether the object can load a specified type of media resource.


## -parameters




### -param AudioOnly [in]

If <b>TRUE</b>, the Media Engine is set to audio-only mode. Otherwise, the Media Engine is set to audio-video mode.


### -param MimeType [in]

A string that contains a MIME type with an optional codecs parameter, as defined in RFC 4281.


### -param pAnswer [out]

Receives a member of the <a href="https://msdn.microsoft.com/AABABB09-D45F-474C-B692-DC3592ED164F">MF_MEDIA_ENGINE_CANPLAY</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implement this method if your Media Engine extension supports one or more MIME types.




## -see-also




<a href="https://msdn.microsoft.com/A032E0D0-2201-4B81-9FE0-8E9CE2707FDB">IMFMediaEngineExtension</a>
 

 

