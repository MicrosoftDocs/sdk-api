---
UID: NF:vfw.AVIStreamFindSample
title: AVIStreamFindSample function
author: windows-sdk-content
description: The AVIStreamFindSample function returns the position of a sample (key frame, nonempty frame, or a frame containing a format change) relative to the specified position.
old-location: multimedia\avistreamfindsample.htm
old-project: Multimedia
ms.assetid: 2bd89f50-0d3a-4c34-b7b8-dc29f2d54d55
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: AVIStreamFindSample, AVIStreamFindSample function [Windows Multimedia], _win32_AVIStreamFindSample, multimedia.avistreamfindsample, vfw/AVIStreamFindSample
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Avifil32.dll
api_name:
-	AVIStreamFindSample
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
req.product: Windows UI
---

# AVIStreamFindSample function


## -description



The <b>AVIStreamFindSample</b> function returns the position of a sample (key frame, nonempty frame, or a frame containing a format change) relative to the specified position.



This function supersedes the obsolete <b>AVIStreamFindKeyFrame</b> function.


## -parameters




### -param pavi

Handle to an open stream.


### -param lPos

Starting frame for the search.


### -param lFlags

Flags that designate the type of frame to locate, the direction in the stream to search, and the type of return information. The following flags are defined.

<table>
<tr>
<th>
Value
</th>
<th>
Meaning
</th>
</tr>
<tr>
<td>FIND_ANY</td>
<td>Finds a nonempty frame. This flag supersedes the SEARCH_ANY flag.</td>
</tr>
<tr>
<td>FIND_KEY</td>
<td>Finds a key frame. This flag supersedes the SEARCH_KEY flag.</td>
</tr>
<tr>
<td>FIND_FORMAT</td>
<td>Finds a format change.</td>
</tr>
<tr>
<td>FIND_NEXT</td>
<td>Finds nearest sample, frame, or format change searching forward. The current sample is included in the search. Use this flag with the FIND_ANY, FIND_KEY, or FIND_FORMAT flag. This flag supersedes the SEARCH_FORWARD flag.</td>
</tr>
<tr>
<td>FIND_PREV</td>
<td>Finds nearest sample, frame, or format change searching backward. The current sample is included in the search. Use this flag with the FIND_ANY, FIND_KEY, or FIND_FORMAT flag. This flag supersedes the SEARCH_NEAREST and SEARCH_BACKWARD flags.</td>
</tr>
<tr>
<td>FIND_FROM_START</td>
<td>Finds first sample, frame, or format change beginning from the start of the stream. Use this flag with the FIND_ANY, FIND_KEY, or FIND_FORMAT flag.</td>
</tr>
</table>
 


## -returns



Returns the position of the frame found or -1 if the search is unsuccessful.




## -remarks



The FIND_KEY, FIND_ANY, and FIND_FORMAT flags are mutually exclusive, as are the FIND_NEXT and FIND_PREV flags.

The argument <i>pavi</i> contains a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

