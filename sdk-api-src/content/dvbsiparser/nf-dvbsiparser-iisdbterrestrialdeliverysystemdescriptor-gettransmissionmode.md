---
UID: NF:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor.GetTransmissionMode
title: IIsdbTerrestrialDeliverySystemDescriptor::GetTransmissionMode
author: windows-sdk-content
description: Gets the transmission mode from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor_gettransmissionmode.htm
old-project: mstv
ms.assetid: d7f4659f-0aa6-46a6-a352-da801d132866
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetTransmissionMode, GetTransmissionMode method [Microsoft TV Technologies], GetTransmissionMode method [Microsoft TV Technologies],IIsdbTerrestrialDeliverySystemDescriptor interface, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetTransmissionMode method, IIsdbTerrestrialDeliverySystemDescriptor.GetTransmissionMode, IIsdbTerrestrialDeliverySystemDescriptor::GetTransmissionMode, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetTransmissionMode, mstv.iisdbterrestrialdeliverysystemdescriptor_gettransmissionmode
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbTerrestrialDeliverySystemDescriptor.GetTransmissionMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbTerrestrialDeliverySystemDescriptor::GetTransmissionMode


## -description


 Gets the transmission mode from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.


## -parameters




### -param pbVal [out]

Receives a code indicating the transmission mode. This code can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>00</dt>
</dl>
</td>
<td width="60%">
Mode 1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>01</dt>
</dl>
</td>
<td width="60%">
Mode 2.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Mode 3.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/32bde3dd-05e0-466b-9f04-4b55b0d7f374">IIsdbTerrestrialDeliverySystemDescriptor</a>
 

 

