---
UID: NF:dvbsiparser.IDVB_TOT.GetUTCTime
title: IDVB_TOT::GetUTCTime
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_tot_getutctime.htm
tech.root: MSTV
ms.assetid: 67092908-b2bb-4dc6-8fb4-d45b03823c69
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetUTCTime, GetUTCTime method [Microsoft TV Technologies], GetUTCTime method [Microsoft TV Technologies],IDVB_TOT interface, IDVB_TOT interface [Microsoft TV Technologies],GetUTCTime method, IDVB_TOT.GetUTCTime, IDVB_TOT::GetUTCTime, IDVB_TOTGetUTCTime, dvbsiparser/IDVB_TOT::GetUTCTime, mstv.idvb_tot_getutctime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
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
 - dvbsiparser.h
api_name:
 - IDVB_TOT.GetUTCTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_TOT::GetUTCTime


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetUTCTime</b> method returns the current UTC time and date.


## -parameters




### -param pmdtVal [out]

Pointer to an <a href="https://msdn.microsoft.com/586269c5-3415-4a5c-8c8f-b405a7bc3f56">MPEG_DATE_AND_TIME</a> structure allocated by the caller. The method fills the structure with the UTC time and date.


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




<a href="https://msdn.microsoft.com/fe5b6b7c-fc6b-4889-b780-4b9f61f3e895">IDVB_TOT Interface</a>
 

 

