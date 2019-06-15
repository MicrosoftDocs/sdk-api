---
UID: NF:dvbsiparser.IDvbTerrestrialDeliverySystemDescriptor.GetCodeRateLPStream
title: IDvbTerrestrialDeliverySystemDescriptor::GetCodeRateLPStream (dvbsiparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbterrestrialdeliverysystemdescriptor_getcoderatelpstream.htm
tech.root: mstv
ms.assetid: dc4a1eef-1dd3-4946-8dad-6c8993290ca2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCodeRateLPStream, GetCodeRateLPStream method [Microsoft TV Technologies], GetCodeRateLPStream method [Microsoft TV Technologies],IDvbTerrestrialDeliverySystemDescriptor interface, IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetCodeRateLPStream method, IDvbTerrestrialDeliverySystemDescriptor.GetCodeRateLPStream, IDvbTerrestrialDeliverySystemDescriptor::GetCodeRateLPStream, IDvbTerrestrialDeliverySystemDescriptorGetCodeRateLPStream, dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor::GetCodeRateLPStream, mstv.idvbterrestrialdeliverysystemdescriptor_getcoderatelpstream
ms.topic: method
f1_keywords: ["dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor.GetCodeRateLPStream"]
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
 - IDvbTerrestrialDeliverySystemDescriptor.GetCodeRateLPStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbTerrestrialDeliverySystemDescriptor::GetCodeRateLPStream


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetCodeRateLPStream</b> method returns the code rate for the low-priority (LP) stream.


## -parameters




### -param pbVal [out]

Receives the code_rate-LP_stream field.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbterrestrialdeliverysystemdescriptor">IDvbTerrestrialDeliverySystemDescriptor Interface</a>
 

 

