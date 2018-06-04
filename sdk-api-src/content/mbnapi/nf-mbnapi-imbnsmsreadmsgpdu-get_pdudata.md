---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMbnSmsReadMsgPdu::get_PduData


## -description


The PDU message in hexadecimal format as used by GSM devices.

This property is read-only.


## -parameters


## -remarks



  For GSM devices, this data in <i>PduData</i> is compliant to the PDU structure defined in 3GPP TS 27.005 and 3GPP TS 23.040.

The table below shows an example of how a PDU message containing the message "Hello" would be structured.


<table>
<tr>
<th>Example</th>
<td>07</td>
<td>91198994000010</td>
<td>11000A9189945086180000AA05C8329BFD06</td>
</tr>
<tr>
<th>Contents</th>
<td>Size of Service Center Address</td>
<td>Service Center Address</td>
<td>PDU in hexadecimal format</td>
</tr>
<tr>
<th>Size</th>
<td>1 byte</td>
<td>Variable</td>
<td>Variable</td>
</tr>
</table>
 



For CDMA devices, this property returns <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/dc0e15c4-6203-4105-9d19-5931b27047d2">IMbnSmsReadMsgPdu</a>
 

 

