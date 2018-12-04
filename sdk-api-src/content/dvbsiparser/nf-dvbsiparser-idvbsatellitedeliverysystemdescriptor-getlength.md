---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetLength
title: IDvbSatelliteDeliverySystemDescriptor::GetLength
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getlength.htm
tech.root: mstv
ms.assetid: dd3ce6ba-e9a7-495d-80e7-532e5cf5e94c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbSatelliteDeliverySystemDescriptor.GetLength, IDvbSatelliteDeliverySystemDescriptor::GetLength, IDvbSatelliteDeliverySystemDescriptorGetLength, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetLength, mstv.idvbsatellitedeliverysystemdescriptor_getlength
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
 - IDvbSatelliteDeliverySystemDescriptor.GetLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSatelliteDeliverySystemDescriptor::GetLength


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetLength</b> method returns the length of the descriptor body.


## -parameters




### -param pbVal [out]

Receives the length of the descriptor body, in bytes.


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
 

 

