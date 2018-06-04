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

# _WMSynchronisedLyrics structure


## -description



The <b>WM_SYNCHRONISED_LYRICS</b> structure is used as the data item for the <a href="https://msdn.microsoft.com/edc73826-9062-4767-8659-8ec4652c42ab">WM/Lyrics_Synchronised</a> complex metadata attribute.




## -struct-fields




### -field bTimeStampFormat

<b>BYTE</b> specifying the format of time stamps in the lyrics. Set to one of the following values.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>1</td>
<td>Time stamps are 32-bit values containing the absolute time of the lyric in frame numbers.</td>
</tr>
<tr>
<td>2</td>
<td>Time stamps are 32-bit values containing the absolute time of the lyric in milliseconds.</td>
</tr>
</table>
 




### -field bContentType

<b>BYTE</b> specifying the type of synchronized strings that are in the lyrics data. Set to one of the following values.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Synchronized strings other than the types listed in this table</td>
</tr>
<tr>
<td>1</td>
<td>Song lyrics</td>
</tr>
<tr>
<td>2</td>
<td>Text transcription</td>
</tr>
<tr>
<td>3</td>
<td>Names of parts of the content. For example, movements of classical pieces, like "Adagio"</td>
</tr>
<tr>
<td>4</td>
<td>Events, such as stage directions in operas</td>
</tr>
<tr>
<td>5</td>
<td>Chord notations</td>
</tr>
<tr>
<td>6</td>
<td>Trivia information</td>
</tr>
<tr>
<td>7</td>
<td>URLs to Web pages</td>
</tr>
<tr>
<td>8</td>
<td>URLs to images</td>
</tr>
</table>
 




### -field pwszContentDescriptor

Pointer to a wide-character null-terminated string containing data from the encoding application. An individual application can use this member in any way desired.


### -field dwLyricsLen

<b>DWORD</b> containing the length, in bytes, of the lyric data pointed to by <b>pbLyrics</b>.


### -field pbLyrics

Pointer to a <b>BYTE</b> array containing the lyrics. You can break the lyrics into syllables, or divide them in some other way that suits the needs of your application. Each syllable or part is included as a null-terminated, wide-character string followed by a 32-bit time stamp. The unit of measurement for the time stamp is determined by the value of <b>bTimeStampFormat</b>.


## -remarks



The objects of the Windows Media Format SDK do not validate the values of time stamps for synchronized lyrics. However, the data is checked to ensure that there is a time stamp for every string, and that the data alternates between strings and integers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

