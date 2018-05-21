---
UID: NF:dvbsiparser.IDvbCableDeliverySystemDescriptor.GetFECInner
title: IDvbCableDeliverySystemDescriptor::GetFECInner
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbcabledeliverysystemdescriptor_getfecinner.htm
old-project: mstv
ms.assetid: 6b16b904-58aa-4f28-83aa-80dd625d387a
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetFECInner, GetFECInner method [Microsoft TV Technologies], GetFECInner method [Microsoft TV Technologies],IDvbCableDeliverySystemDescriptor interface, IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies],GetFECInner method, IDvbCableDeliverySystemDescriptor.GetFECInner, IDvbCableDeliverySystemDescriptor::GetFECInner, IDvbCableDeliverySystemDescriptorGetFECInner, dvbsiparser/IDvbCableDeliverySystemDescriptor::GetFECInner, mstv.idvbcabledeliverysystemdescriptor_getfecinner
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
-	IDvbCableDeliverySystemDescriptor.GetFECInner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbCableDeliverySystemDescriptor::GetFECInner


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




<a href="https://msdn.microsoft.com/b4fb2fd0-e32a-4737-8095-7d4df40a26a0">IDvbCableDeliverySystemDescriptor Interface</a>
 

 

