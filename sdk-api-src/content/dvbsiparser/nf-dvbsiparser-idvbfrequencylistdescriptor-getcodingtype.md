---
UID: NF:dvbsiparser.IDvbFrequencyListDescriptor.GetCodingType
title: IDvbFrequencyListDescriptor::GetCodingType
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbfrequencylistdescriptor_getcodingtype.htm
old-project: mstv
ms.assetid: 0d458f42-bea5-4503-a2d7-89efd1abc1a8
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCodingType, GetCodingType method [Microsoft TV Technologies], GetCodingType method [Microsoft TV Technologies],IDvbFrequencyListDescriptor interface, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],GetCodingType method, IDvbFrequencyListDescriptor.GetCodingType, IDvbFrequencyListDescriptor::GetCodingType, IDvbFrequencyListDescriptorGetCodingType, dvbsiparser/IDvbFrequencyListDescriptor::GetCodingType, mstv.idvbfrequencylistdescriptor_getcodingtype
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
-	IDvbFrequencyListDescriptor.GetCodingType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbFrequencyListDescriptor::GetCodingType


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCodingType</b> method returns a flag that specifies how the frequency is coded.


## -parameters




### -param pbVal [out]

Receives the coding_type flag.


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
 

 

