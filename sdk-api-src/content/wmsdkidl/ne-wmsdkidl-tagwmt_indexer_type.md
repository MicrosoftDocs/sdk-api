---
UID: NE:wmsdkidl.tagWMT_INDEXER_TYPE
title: tagWMT_INDEXER_TYPE
author: windows-driver-content
description: The WMT_INDEXER_TYPE enumeration type defines the types of indexing supported by the indexer.
old-location: wmformat\wmt_indexer_type.htm
old-project: wmformat
ms.assetid: 1b80511c-175f-4d05-8ce6-d048a9e77223
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WMT_INDEXER_TYPE, WMT_INDEXER_TYPE enumeration [windows Media Format], WMT_IT_FRAME_NUMBERS, WMT_IT_PRESENTATION_TIME, WMT_IT_TIMECODE, tagWMT_INDEXER_TYPE, wmformat.wmt_indexer_type, wmsdkidl/WMT_INDEXER_TYPE, wmsdkidl/WMT_IT_FRAME_NUMBERS, wmsdkidl/WMT_IT_PRESENTATION_TIME, wmsdkidl/WMT_IT_TIMECODE
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
req.typenames: WMT_INDEXER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmsdkidl.h
api_name:
-	WMT_INDEXER_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagWMT_INDEXER_TYPE enumeration


## -description



The <b>WMT_INDEXER_TYPE</b> enumeration type defines the types of indexing supported by the indexer.




## -enum-fields




### -field WMT_IT_PRESENTATION_TIME

The indexer will construct an index using presentation times as indexes.


### -field WMT_IT_FRAME_NUMBERS

The indexer will construct an index using frame numbers as indexes.


### -field WMT_IT_TIMECODE

The indexer will construct an index using SMPTE time codes as indexes.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

