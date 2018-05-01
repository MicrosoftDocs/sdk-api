---
UID: NF:dvbsiparser.IDVB_EIT2.GetRecordSection
title: IDVB_EIT2::GetRecordSection method
author: windows-driver-content
description: Gets the number of a section containing an event information table (EIT) record.
old-location: mstv\idvb_eit2_getrecordsection.htm
old-project: mstv
ms.assetid: 249c93f2-53d7-4110-9db3-34f3b0296b48
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordSection method [Microsoft TV Technologies], GetRecordSection method [Microsoft TV Technologies], IDVB_EIT2 interface, GetRecordSection,IDVB_EIT2.GetRecordSection, IDVB_EIT2, IDVB_EIT2 interface [Microsoft TV Technologies], GetRecordSection method, IDVB_EIT2::GetRecordSection, dvbsiparser/IDVB_EIT2::GetRecordSection, mstv.idvb_eit2_getrecordsection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDVB_EIT2.GetRecordSection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_EIT2::GetRecordSection method


## -description


Gets the number of a section containing an event information table (EIT) record.


## -parameters




### -param dwRecordIndex [in]

The record number, indexed from 0. Call <a href="https://msdn.microsoft.com/1ea8c91b-f1a2-4c04-933c-c8a2fbfda86f">IDVB_EIT::GetCountOfRecords</a> to get the number of records in the EIT.


### -param pbVal [out]

Receives the number of the section containing the specified record. A value of 0 indicates the present section; a value of 1 indicates the following section.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
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
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method was not called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9d93130c-12fb-4c76-98c1-cdfae113cf2c">IDVB_EIT2</a>
 

 

