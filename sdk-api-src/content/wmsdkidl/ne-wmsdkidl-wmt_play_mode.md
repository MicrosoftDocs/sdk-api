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

# WMT_PLAY_MODE enumeration


## -description



The <b>WMT_PLAY_MODE</b> enumeration type defines the playback options of the reader.




## -enum-fields




### -field WMT_PLAY_MODE_AUTOSELECT

The reader will select the most appropriate play mode based on the location of the content.


### -field WMT_PLAY_MODE_LOCAL

The reader will read files from a local storage location.


### -field WMT_PLAY_MODE_DOWNLOAD

The reader will download files from network locations.


### -field WMT_PLAY_MODE_STREAMING

The reader will stream files from network locations.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/06bff83f-c3f2-4eca-85dd-7e7b93cfd73d">IWMReaderAdvanced2::GetDownloadProgress</a>



<a href="https://msdn.microsoft.com/45c7e2c2-fff4-41a9-b5ce-76d8d6257e77">IWMReaderAdvanced2::GetPlayMode</a>



<a href="https://msdn.microsoft.com/97bdac1f-8830-45c0-9229-322ad72b3954">IWMReaderAdvanced2::SaveFileAs</a>



<a href="https://msdn.microsoft.com/d1b20a0c-fedf-46d4-a76b-7596dcf8fcf8">IWMReaderAdvanced2::SetPlayMode</a>
 

 

