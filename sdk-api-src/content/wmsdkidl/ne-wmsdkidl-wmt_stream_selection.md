---
UID: NE:wmsdkidl.WMT_STREAM_SELECTION
title: WMT_STREAM_SELECTION
author: windows-sdk-content
description: The WMT_STREAM_SELECTION enumeration type defines the playback status of a stream.
old-location: wmformat\wmt_stream_selection.htm
old-project: wmformat
ms.assetid: 7191d608-1a25-48c0-858b-c5e93f9d8e6e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WMT_CLEANPOINT_ONLY, WMT_OFF, WMT_ON, WMT_STREAM_SELECTION, WMT_STREAM_SELECTION enumeration [windows Media Format], wmformat.wmt_stream_selection, wmsdkidl/WMT_CLEANPOINT_ONLY, wmsdkidl/WMT_OFF, wmsdkidl/WMT_ON, wmsdkidl/WMT_STREAM_SELECTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
req.typenames: WMT_STREAM_SELECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_STREAM_SELECTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMT_STREAM_SELECTION enumeration


## -description



The <b>WMT_STREAM_SELECTION</b> enumeration type defines the playback status of a stream.




## -enum-fields




### -field WMT_OFF

No samples will be delivered for the stream.


### -field WMT_CLEANPOINT_ONLY

Only samples with <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">cleanpoints</a> will be delivered for the stream.


### -field WMT_ON

All samples will be delivered for the stream.


## -see-also




<a href="https://msdn.microsoft.com/cd28f608-25ba-44a7-868b-b1cd4dfcfa45">Enumeration Types</a>
 

 

