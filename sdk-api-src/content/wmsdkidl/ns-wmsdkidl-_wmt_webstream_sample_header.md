---
UID: NS:wmsdkidl._WMT_WEBSTREAM_SAMPLE_HEADER
title: "_WMT_WEBSTREAM_SAMPLE_HEADER"
author: windows-sdk-content
description: The WMT_WEBSTREAM_SAMPLE_HEADER structure is used as a variable-sized header for each Web stream sample.
old-location: wmformat\wmt_webstream_sample_header.htm
old-project: wmformat
ms.assetid: 5492af92-4829-4bf1-8512-3d57fbe70ce5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WMT_WEBSTREAM_SAMPLE_HEADER, WMT_WEBSTREAM_SAMPLE_HEADER structure [windows Media Format], _WMT_WEBSTREAM_SAMPLE_HEADER, wmformat.wmt_webstream_sample_header, wmsdkidl/WMT_WEBSTREAM_SAMPLE_HEADER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WMT_WEBSTREAM_SAMPLE_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_WEBSTREAM_SAMPLE_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WMT_WEBSTREAM_SAMPLE_HEADER structure


## -description



The <b>WMT_WEBSTREAM_SAMPLE_HEADER</b> structure is used as a variable-sized header for each Web stream sample.




## -struct-fields




### -field cbLength

<b>WORD</b> containing the size of <b>wszURL</b> in wide characters.


### -field wPart

<b>WORD</b> containing the zero-based part number to which the sample applies. When the last part is received, <b>wPart</b> equals <b>cTotalParts</b>– 1.


### -field cTotalParts

<b>WORD</b> containing the total number of parts in the Web stream.


### -field wSampleType

<b>WORD</b> containing the type of Web stream, either WEBSTREAM_SAMPLE_TYPE_FILE (0x1) or WEBSTREAM_SAMPLE_TYPE_RENDER (0x2). See Remarks.


### -field wszURL

Wide-character null-terminated string specifying the local URL.


## -remarks



In a Web stream, each sample begins with this structure. The application is responsible for determining the size of the structure for each sample delivered. The size depends on the length of the <b>wszURL</b> member, as reported in the <b>cbLength</b> member.

If <b>wSampleType</b> is WEBSTREAM_SAMPLE_TYPE_FILE, the sample contains data immediately following the header that should be cached for later rendering. If the type is WEBSTREAM_SAMPLE_TYPE_RENDER, the sample contains no data. The application should cause the file named in the <b>wszURL</b> member to be immediately rendered on the display.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

