---
UID: NE:wmsdkidl.tagWMT_OFFSET_FORMAT
title: tagWMT_OFFSET_FORMAT
author: windows-driver-content
description: The WMT_OFFSET_FORMAT enumeration type defines the types of offsets used in this SDK.
old-location: wmformat\wmt_offset_format.htm
old-project: wmformat
ms.assetid: b4119098-0407-462b-8550-46f8c1312fe0
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WMT_OFFSET_FORMAT, WMT_OFFSET_FORMAT enumeration [windows Media Format], WMT_OFFSET_FORMAT_100NS, WMT_OFFSET_FORMAT_100NS_APPROXIMATE, WMT_OFFSET_FORMAT_FRAME_NUMBERS, WMT_OFFSET_FORMAT_PLAYLIST_OFFSET, WMT_OFFSET_FORMAT_TIMECODE, tagWMT_OFFSET_FORMAT, wmformat.wmt_offset_format, wmsdkidl/WMT_OFFSET_FORMAT, wmsdkidl/WMT_OFFSET_FORMAT_100NS, wmsdkidl/WMT_OFFSET_FORMAT_100NS_APPROXIMATE, wmsdkidl/WMT_OFFSET_FORMAT_FRAME_NUMBERS, wmsdkidl/WMT_OFFSET_FORMAT_PLAYLIST_OFFSET, wmsdkidl/WMT_OFFSET_FORMAT_TIMECODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.typenames: WMT_OFFSET_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmsdkidl.h
api_name:
-	WMT_OFFSET_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagWMT_OFFSET_FORMAT enumeration


## -description



The <b>WMT_OFFSET_FORMAT</b> enumeration type defines the types of offsets used in this SDK.




## -enum-fields




### -field WMT_OFFSET_FORMAT_100NS

An offset into a file is specified by presentation time in 100-nanosecond units.


### -field WMT_OFFSET_FORMAT_FRAME_NUMBERS

An offset into a file is specified by frame number.


### -field WMT_OFFSET_FORMAT_PLAYLIST_OFFSET

An offset of playlist entries.


### -field WMT_OFFSET_FORMAT_TIMECODE

An offset into a file is specified by presentation time as identified by SMTPE time codes.


### -field WMT_OFFSET_FORMAT_100NS_APPROXIMATE

Used to specify approximate seeking. This type of offset seeks to the closest key frame prior to the time specified.


## -remarks



<b>WMT_OFFSET_FORMAT</b> is used as an input parameter to <a href="https://msdn.microsoft.com/64b922be-3a8f-4cbe-aa1d-aa3833e1f0fa">IWMReaderAdvanced3::StartAtPosition</a>. The value passed specifies whether the reader should begin playback at a specified presentation time, frame number, or offset into a playlist.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

