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
 

 

