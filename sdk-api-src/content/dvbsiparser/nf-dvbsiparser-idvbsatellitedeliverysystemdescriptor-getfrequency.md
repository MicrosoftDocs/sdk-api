---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetFrequency
title: IDvbSatelliteDeliverySystemDescriptor::GetFrequency
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getfrequency.htm
tech.root: mstv
ms.assetid: dc298f61-f7f1-42dc-a585-bfe9f58b1629
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFrequency, GetFrequency method [Microsoft TV Technologies], GetFrequency method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetFrequency method, IDvbSatelliteDeliverySystemDescriptor.GetFrequency, IDvbSatelliteDeliverySystemDescriptor::GetFrequency, IDvbSatelliteDeliverySystemDescriptorGetFrequency, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetFrequency, mstv.idvbsatellitedeliverysystemdescriptor_getfrequency
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
 - IDvbSatelliteDeliverySystemDescriptor.GetFrequency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSatelliteDeliverySystemDescriptor::GetFrequency


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetFrequency</b> method returns the frequency.


## -parameters




### -param pdwVal [out]

Receives the frequency field.


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




<a href="https://msdn.microsoft.com/814becf0-c98a-4419-aca6-d9b22d273e97">IDvbSatelliteDeliverySystemDescriptor Interface</a>
 

 

