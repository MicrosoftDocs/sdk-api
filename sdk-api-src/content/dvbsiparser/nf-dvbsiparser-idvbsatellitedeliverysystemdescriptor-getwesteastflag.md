---
UID: NF:dvbsiparser.IDvbSatelliteDeliverySystemDescriptor.GetWestEastFlag
title: IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbsatellitedeliverysystemdescriptor_getwesteastflag.htm
old-project: mstv
ms.assetid: 533a2ed4-f5ac-4f41-a03b-0b274f327436
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetWestEastFlag, GetWestEastFlag method [Microsoft TV Technologies], GetWestEastFlag method [Microsoft TV Technologies],IDvbSatelliteDeliverySystemDescriptor interface, IDvbSatelliteDeliverySystemDescriptor interface [Microsoft TV Technologies],GetWestEastFlag method, IDvbSatelliteDeliverySystemDescriptor.GetWestEastFlag, IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag, IDvbSatelliteDeliverySystemDescriptorGetWestEastFlag, dvbsiparser/IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag, mstv.idvbsatellitedeliverysystemdescriptor_getwesteastflag
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
 - IDvbSatelliteDeliverySystemDescriptor.GetWestEastFlag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbSatelliteDeliverySystemDescriptor::GetWestEastFlag


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetWestEastFlag</b> method returns a flag that specifies whether the satellite is in the western or eastern part of the orbit.


## -parameters




### -param pbVal [out]

Receives the west_east_flag field.


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
 

 

