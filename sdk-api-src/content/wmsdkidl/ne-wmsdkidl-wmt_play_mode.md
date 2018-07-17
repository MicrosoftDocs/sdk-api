---
UID: NE:wmsdkidl.WMT_PLAY_MODE
title: WMT_PLAY_MODE
author: windows-sdk-content
description: The WMT_PLAY_MODE enumeration type defines the playback options of the reader.
old-location: wmformat\wmt_play_mode.htm
old-project: wmformat
ms.assetid: da47fc9f-7762-4f92-8857-44a75a4cd00b
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: WMT_PLAY_MODE, WMT_PLAY_MODE enumeration [windows Media Format], WMT_PLAY_MODE_AUTOSELECT, WMT_PLAY_MODE_DOWNLOAD, WMT_PLAY_MODE_LOCAL, WMT_PLAY_MODE_STREAMING, enumeration [windows Media Format], wmformat.wmt_play_mode, wmsdkidl/WMT_PLAY_MODE, wmsdkidl/WMT_PLAY_MODE_AUTOSELECT, wmsdkidl/WMT_PLAY_MODE_DOWNLOAD, wmsdkidl/WMT_PLAY_MODE_LOCAL, wmsdkidl/WMT_PLAY_MODE_STREAMING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WMT_PLAY_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_PLAY_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

