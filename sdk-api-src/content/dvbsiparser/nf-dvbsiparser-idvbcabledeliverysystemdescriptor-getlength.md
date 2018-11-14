---
UID: NF:dvbsiparser.IDvbCableDeliverySystemDescriptor.GetLength
title: IDvbCableDeliverySystemDescriptor::GetLength
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvbcabledeliverysystemdescriptor_getlength.htm
tech.root: MSTV
ms.assetid: 9f6c0a4c-6f0e-4217-b6a0-af709a75d24d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbCableDeliverySystemDescriptor interface, IDvbCableDeliverySystemDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbCableDeliverySystemDescriptor.GetLength, IDvbCableDeliverySystemDescriptor::GetLength, IDvbCableDeliverySystemDescriptorGetLength, dvbsiparser/IDvbCableDeliverySystemDescriptor::GetLength, mstv.idvbcabledeliverysystemdescriptor_getlength
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
 - IDvbCableDeliverySystemDescriptor.GetLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IDvbCableDeliverySystemDescriptor.GetLength
: 
---

# IDvbCableDeliverySystemDescriptor::GetLength


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




<a href="https://msdn.microsoft.com/b4fb2fd0-e32a-4737-8095-7d4df40a26a0">IDvbCableDeliverySystemDescriptor Interface</a>
 

 

