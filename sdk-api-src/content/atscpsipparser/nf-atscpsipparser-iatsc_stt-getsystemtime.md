---
UID: NF:atscpsipparser.IATSC_STT.GetSystemTime
title: IATSC_STT::GetSystemTime (atscpsipparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_stt_getsystemtime.htm
tech.root: mstv
ms.assetid: 4add19d8-9626-468f-8b15-993fb51f3c13
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSystemTime, GetSystemTime method [Microsoft TV Technologies], GetSystemTime method [Microsoft TV Technologies],IATSC_STT interface, IATSC_STT interface [Microsoft TV Technologies],GetSystemTime method, IATSC_STT.GetSystemTime, IATSC_STT::GetSystemTime, IATSC_STTGetSystemTime, atscpsipparser/IATSC_STT::GetSystemTime, mstv.iatsc_stt_getsystemtime
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
 - IATSC_STT.GetSystemTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSC_STT::GetSystemTime


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSystemTime</b> method returns the current system time.


## -parameters




### -param pmdtSystemTime [out]

Pointer to an <a href="https://msdn.microsoft.com/586269c5-3415-4a5c-8c8f-b405a7bc3f56">MPEG_DATE_AND_TIME</a> structure allocated by the caller. The method fills the structure with the system time.


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
 




## -see-also




<a href="https://msdn.microsoft.com/03e903e0-e722-42c6-b6b7-448fecc379b9">IATSC_STT Interface</a>
 

 

