---
UID: NF:dvbsiparser.IDvbTerrestrialDeliverySystemDescriptor.GetCentreFrequency
title: IDvbTerrestrialDeliverySystemDescriptor::GetCentreFrequency
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbterrestrialdeliverysystemdescriptor_getcentrefrequency.htm
old-project: mstv
ms.assetid: 80ce6831-afb0-4fdd-844d-1aa400449110
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCentreFrequency, GetCentreFrequency method [Microsoft TV Technologies], GetCentreFrequency method [Microsoft TV Technologies],IDvbTerrestrialDeliverySystemDescriptor interface, IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetCentreFrequency method, IDvbTerrestrialDeliverySystemDescriptor.GetCentreFrequency, IDvbTerrestrialDeliverySystemDescriptor::GetCentreFrequency, IDvbTerrestrialDeliverySystemDescriptorGetCentreFrequency, dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor::GetCentreFrequency, mstv.idvbterrestrialdeliverysystemdescriptor_getcentrefrequency
ms.prod: windows
ms.technology: windows-sdk
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
-	IDvbTerrestrialDeliverySystemDescriptor.GetCentreFrequency
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbTerrestrialDeliverySystemDescriptor::GetCentreFrequency


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCentreFrequency</b> method returns the center frequency.


## -parameters




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




<a href="https://msdn.microsoft.com/7000f937-2f58-43c1-b0e1-60d3171485b0">IDvbTerrestrialDeliverySystemDescriptor Interface</a>
 

 

