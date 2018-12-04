---
UID: NF:atscpsipparser.IATSC_STT.GetGpsUtcOffset
title: IATSC_STT::GetGpsUtcOffset
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_stt_getgpsutcoffset.htm
tech.root: mstv
ms.assetid: 124c864a-a504-4f3c-836f-bdbe730beda7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetGpsUtcOffset, GetGpsUtcOffset method [Microsoft TV Technologies], GetGpsUtcOffset method [Microsoft TV Technologies],IATSC_STT interface, IATSC_STT interface [Microsoft TV Technologies],GetGpsUtcOffset method, IATSC_STT.GetGpsUtcOffset, IATSC_STT::GetGpsUtcOffset, IATSC_STTGetGpsUtcOffset, atscpsipparser/IATSC_STT::GetGpsUtcOffset, mstv.iatsc_stt_getgpsutcoffset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_STT.GetGpsUtcOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSC_STT::GetGpsUtcOffset


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetGpsUtcOffset</b> method returns the current offset between Global Positioning Satellite (GPS) time and Universal Time Coordinated (UTC), in seconds.


## -parameters




### -param pbVal [out]

Receives the GPS_UTC_offset field.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



GPS time is measured in seconds since January 6, 1980, and is not adjusted for leap seconds. To convert GPS time to UTC, which is adjusted for leap seconds, subtract the offset from GPS time.




## -see-also




<a href="https://msdn.microsoft.com/03e903e0-e722-42c6-b6b7-448fecc379b9">IATSC_STT Interface</a>
 

 

