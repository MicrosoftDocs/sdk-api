---
UID: NF:dvbsiparser.IDvbTerrestrialDeliverySystemDescriptor.GetTransmissionMode
title: IDvbTerrestrialDeliverySystemDescriptor::GetTransmissionMode method
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbterrestrialdeliverysystemdescriptor_gettransmissionmode.htm
old-project: mstv
ms.assetid: d825f933-0da6-4e8e-bc28-b9e2db575a12
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTransmissionMode method [Microsoft TV Technologies], GetTransmissionMode method [Microsoft TV Technologies], IDvbTerrestrialDeliverySystemDescriptor interface, GetTransmissionMode,IDvbTerrestrialDeliverySystemDescriptor.GetTransmissionMode, IDvbTerrestrialDeliverySystemDescriptor, IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies], GetTransmissionMode method, IDvbTerrestrialDeliverySystemDescriptor::GetTransmissionMode, IDvbTerrestrialDeliverySystemDescriptorGetTransmissionMode, dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor::GetTransmissionMode, mstv.idvbterrestrialdeliverysystemdescriptor_gettransmissionmode
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
-	IDvbTerrestrialDeliverySystemDescriptor.GetTransmissionMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbTerrestrialDeliverySystemDescriptor::GetTransmissionMode method


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTransmissionMode</b> method returns the transmission mode.


## -parameters




### -param pbVal [out]

Receives the transmission_mode field.


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
 

 

