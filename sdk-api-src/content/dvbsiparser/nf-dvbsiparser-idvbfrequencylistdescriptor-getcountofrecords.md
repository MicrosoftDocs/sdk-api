---
UID: NF:dvbsiparser.IDvbFrequencyListDescriptor.GetCountOfRecords
title: IDvbFrequencyListDescriptor::GetCountOfRecords
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbfrequencylistdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 9bce2abf-2673-49c6-8b87-7c8825544156
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IDvbFrequencyListDescriptor interface, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IDvbFrequencyListDescriptor.GetCountOfRecords, IDvbFrequencyListDescriptor::GetCountOfRecords, IDvbFrequencyListDescriptorGetCountOfRecords, dvbsiparser/IDvbFrequencyListDescriptor::GetCountOfRecords, mstv.idvbfrequencylistdescriptor_getcountofrecords
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
 - IDvbFrequencyListDescriptor.GetCountOfRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbFrequencyListDescriptor::GetCountOfRecords


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCountOfRecords</b> method returns the number of records in the frequency list descriptor.


## -parameters




### -param pbVal [out]

Receives the number of records.


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
 

 

