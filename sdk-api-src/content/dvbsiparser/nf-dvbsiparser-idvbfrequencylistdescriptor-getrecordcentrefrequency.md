---
UID: NF:dvbsiparser.IDvbFrequencyListDescriptor.GetRecordCentreFrequency
title: IDvbFrequencyListDescriptor::GetRecordCentreFrequency
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbfrequencylistdescriptor_getrecordcentrefrequency.htm
old-project: mstv
ms.assetid: bb6c3c14-c4b6-412d-ad12-1c7fdb025527
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetRecordCentreFrequency, GetRecordCentreFrequency method [Microsoft TV Technologies], GetRecordCentreFrequency method [Microsoft TV Technologies],IDvbFrequencyListDescriptor interface, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],GetRecordCentreFrequency method, IDvbFrequencyListDescriptor.GetRecordCentreFrequency, IDvbFrequencyListDescriptor::GetRecordCentreFrequency, IDvbFrequencyListDescriptorGetRecordCentreFrequency, dvbsiparser/IDvbFrequencyListDescriptor::GetRecordCentreFrequency, mstv.idvbfrequencylistdescriptor_getrecordcentrefrequency
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbFrequencyListDescriptor.GetRecordCentreFrequency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbFrequencyListDescriptor::GetRecordCentreFrequency


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetRecordCentreFrequency</b> method returns the frequency at a specified index in the frequency list.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the frequency to return. To get the number of frequencies in the descriptor, call <a href="https://msdn.microsoft.com/9bce2abf-2673-49c6-8b87-7c8825544156">IDvbFrequencyListDescriptor::GetCountOfRecords</a>.


### -param pdwVal [out]

Receives the centre_frequency field.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fadf7114-b9e4-4f61-816b-10725b83169a">IDvbFrequencyListDescriptor Interface</a>
 

 

