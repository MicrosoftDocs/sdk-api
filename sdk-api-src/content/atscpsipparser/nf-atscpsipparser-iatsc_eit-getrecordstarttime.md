---
UID: NF:atscpsipparser.IATSC_EIT.GetRecordStartTime
title: IATSC_EIT::GetRecordStartTime
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_eit_getrecordstarttime.htm
tech.root: MSTV
ms.assetid: c403e86c-0579-47a2-ba87-0d2aec2e186c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRecordStartTime, GetRecordStartTime method [Microsoft TV Technologies], GetRecordStartTime method [Microsoft TV Technologies],IATSC_EIT interface, IATSC_EIT interface [Microsoft TV Technologies],GetRecordStartTime method, IATSC_EIT.GetRecordStartTime, IATSC_EIT::GetRecordStartTime, IATSC_EITGetRecordStartTime, atscpsipparser/IATSC_EIT::GetRecordStartTime, mstv.iatsc_eit_getrecordstarttime
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
 - IATSC_EIT.GetRecordStartTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- atscpsipparser.h
: 
- IATSC_EIT.GetRecordStartTime
: 
---

# IATSC_EIT::GetRecordStartTime


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordStartTime</b> method returns the event start time for a record in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call the <a href="https://msdn.microsoft.com/edf16862-5bc4-4022-9727-11c1a291417d">IATSC_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.


### -param pmdtVal [out]

Pointer to an <a href="https://msdn.microsoft.com/586269c5-3415-4a5c-8c8f-b405a7bc3f56">MPEG_DATE_AND_TIME</a> structure allocated by the caller. The method fills the structure with the event start time.


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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

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




<a href="https://msdn.microsoft.com/ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6">IATSC_EIT Interface</a>
 

 

