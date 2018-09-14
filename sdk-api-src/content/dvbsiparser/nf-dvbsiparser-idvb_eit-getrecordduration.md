---
UID: NF:dvbsiparser.IDVB_EIT.GetRecordDuration
title: IDVB_EIT::GetRecordDuration
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_eit_getrecordduration.htm
tech.root: MSTV
ms.assetid: cb480110-0cf4-4b46-af06-f6c42907a184
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetRecordDuration, GetRecordDuration method [Microsoft TV Technologies], GetRecordDuration method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetRecordDuration method, IDVB_EIT.GetRecordDuration, IDVB_EIT::GetRecordDuration, IDVB_EITGetRecordDuration, dvbsiparser/IDVB_EIT::GetRecordDuration, mstv.idvb_eit_getrecordduration
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
 - IDVB_EIT.GetRecordDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_EIT::GetRecordDuration


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordDuration</b> method returns the event duration for a record in the EIT.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. Call <a href="https://msdn.microsoft.com/1ea8c91b-f1a2-4c04-933c-c8a2fbfda86f">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.


### -param pmdVal [out]

Pointer to an <a href="https://msdn.microsoft.com/476b7fe1-2186-4242-9a0b-65ae4e18511e">MPEG_DURATION</a> structure allocated by the caller. The method fills the structure with the event duration.


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




<a href="https://msdn.microsoft.com/86280e1e-09c3-45a4-bdfb-53eda8e5700e">IDVB_EIT Interface</a>
 

 

