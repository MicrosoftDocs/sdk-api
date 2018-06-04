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

# IAMExtendedSeeking::get_ExSeekCapabilities


## -description



The <code>get_ExSeekCapabilities</code> method retrieves the extended seeking capabilities of the filter.




## -parameters




### -param pExCapabilities [out]

Pointer to a variable that receives a bitwise OR of <a href="https://msdn.microsoft.com/f5f21303-3b5b-45e8-a4dc-6c8bc7cd8ad3">AMExtendedSeekingCapabilities</a> flags.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The Windows Media Source filter sets the extended seeking flags as follows.

<table>
<tr>
<td>
              Flag
            </td>
<td>
              Condition
            </td>
</tr>
<tr>
<td>AM_EXSEEK_BUFFERING</td>
<td>Always.</td>
</tr>
<tr>
<td>AM_EXSEEK_NOSTANDARDREPAINT</td>
<td>Always.</td>
</tr>
<tr>
<td>AM_EXSEEK_SENDS_VIDEOFRAMEREADY</td>
<td>If the video pin has been created.</td>
</tr>
<tr>
<td>AM_EXSEEK_CANSCAN, AM_EXSEEK_SCANWITHOUTCLOCK</td>
<td>If the stream supports rates other than 1.0.</td>
</tr>
<tr>
<td>AM_EXSEEK_CANSEEK</td>
<td>If the stream has been authored to be seekable.</td>
</tr>
<tr>
<td>AM_EXSEEK_MARKERSEEK</td>
<td>If the stream contains markers.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9e0e49af-61ef-408c-8c26-bb29ab26a1f5">IAMExtendedSeeking Interface</a>
 

 

