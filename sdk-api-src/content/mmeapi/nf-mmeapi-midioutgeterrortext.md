---
UID: NF:mmeapi.midiOutGetErrorText
title: midiOutGetErrorText function
author: windows-sdk-content
description: The midiOutGetErrorText function retrieves a textual description for an error identified by the specified error code.
old-location: multimedia\midioutgeterrortext.htm
tech.root: Multimedia
ms.assetid: e0e9a22f-da8b-4c87-bbdb-dedc22336503
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_win32_midiOutGetErrorText, midiOutGetErrorText, midiOutGetErrorText function [Windows Multimedia], midiOutGetErrorTextA, midiOutGetErrorTextW, mmeapi/midiOutGetErrorText, mmeapi/midiOutGetErrorTextA, mmeapi/midiOutGetErrorTextW, multimedia.midioutgeterrortext"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: midiOutGetErrorTextW (Unicode) and midiOutGetErrorTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - midiOutGetErrorText
 - midiOutGetErrorTextA
 - midiOutGetErrorTextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- midiOutGetErrorText
: 
---

# midiOutGetErrorText function


## -description



The <b>midiOutGetErrorText</b> function retrieves a textual description for an error identified by the specified error code.




## -parameters




### -param mmrError

Error code.


### -param pszText

Pointer to a buffer to be filled with the textual error description.


### -param cchText

Length, in characters, of the buffer pointed to by <i>lpText</i>.


## -returns



Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_BADERRNUM</b></dt>
</dl>
</td>
<td width="60%">
The specified error number is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified pointer or structure is invalid.

</td>
</tr>
</table>
 




## -remarks



If the textual error description is longer than the specified buffer, the description is truncated. The returned error string is always null-terminated. If <i>cchText</i> is zero, nothing is copied, and the function returns MMSYSERR_NOERROR. All error descriptions are less than MAXERRORLENGTH characters long.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 

