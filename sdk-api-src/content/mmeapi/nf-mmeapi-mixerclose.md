---
UID: NF:mmeapi.mixerClose
title: mixerClose function
author: windows-sdk-content
description: The mixerClose function closes the specified mixer device.
old-location: multimedia\mixerclose.htm
tech.root: Multimedia
ms.assetid: d92a9bb0-9761-471b-85d2-af0bcdbbda34
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "_win32_mixerClose, mixerClose, mixerClose function [Windows Multimedia], mmeapi/mixerClose, multimedia.mixerclose"
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
req.unicode-ansi: 
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
 - mixerClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mixerClose function


## -description



The <b>mixerClose</b> function closes the specified mixer device.




## -parameters




### -param hmx

Handle to the mixer device. This handle must have been returned successfully by the <a href="https://msdn.microsoft.com/7977680b-0967-4b85-9926-fc2725681de9">mixerOpen</a> function. If <b>mixerClose</b> is successful, <i>hmx</i> is no longer valid.


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
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
Specified device handle is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/19f53a98-1a01-4954-a5d7-c428aa2bfa38">Audio Mixer Functions</a>



<a href="https://msdn.microsoft.com/7489fcac-fd4c-46cf-8a1a-e4de576974f0">Audio Mixers</a>
 

 

