---
UID: NS:http._HTTP_BYTE_RANGE
title: "_HTTP_BYTE_RANGE"
author: windows-sdk-content
description: The HTTP_BYTE_RANGE structure is used to specify a byte range within a cached response fragment, file, or other data block.
old-location: http\http_byte_range.htm
tech.root: Http
ms.assetid: a57d23cd-1e91-401a-b242-6549b1457594
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PHTTP_BYTE_RANGE, HTTP_BYTE_RANGE, HTTP_BYTE_RANGE structure [HTTP], PHTTP_BYTE_RANGE, PHTTP_BYTE_RANGE structure pointer [HTTP], _HTTP_BYTE_RANGE, _http_http_byte_range, http.http_byte_range, http/HTTP_BYTE_RANGE, http/PHTTP_BYTE_RANGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Http.h
api_name:
 - HTTP_BYTE_RANGE
product: Windows
targetos: Windows
req.typenames: HTTP_BYTE_RANGE, *PHTTP_BYTE_RANGE
req.redist: 
---

# _HTTP_BYTE_RANGE structure


## -description


The 
<b>HTTP_BYTE_RANGE</b> structure is used to specify a byte range within a cached response fragment, file, or other data block.


## -struct-fields




### -field StartingOffset

Starting offset of the byte range.


### -field Length

Size, in bytes, of the range. If this member is HTTP_BYTE_RANGE_TO_EOF, the range extends from the starting offset to the end of the file or data block.


## -see-also




<a href="https://msdn.microsoft.com/ae67c066-c8bd-483f-829f-30192f49593d">HTTP_DATA_CHUNK</a>



<a href="https://msdn.microsoft.com/2f066e1d-035f-4c1c-b854-de4a6ef58a58">HttpReadFragmentFromCache</a>
 

 

