---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetFECInner
title: IDvbSatelliteDeliverySystemDescriptor::GetFECInner
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getfecinner.htm
old-project: mstv
ms.assetid: fe90fcd7-e77b-42c8-935f-4cf02957400f
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetFECInner, GetFECInner method [Microsoft TV Technologies], GetFECInner method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetFECInner method, IDvbSatelliteDeliverySystemDescriptor.GetFECInner, IDvbSatelliteDeliverySystemDescriptor::GetFECInner, IDvbSatelliteDeliverySystemDescriptorGetFECInner, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetFECInner, mstv.idvbsatellitedeliverysystemdescriptor_getfecinner
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
req.idl: 
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
 - IDvbSatelliteDeliverySystemDescriptor.GetFECInner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbSatelliteDeliverySystemDescriptor::GetFECInner


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetFECInner</b> method returns the inner forward error correction (FEC) scheme.


## -parameters




### -param pbVal [out]

Receives the FEC_inner field.


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
 

 

