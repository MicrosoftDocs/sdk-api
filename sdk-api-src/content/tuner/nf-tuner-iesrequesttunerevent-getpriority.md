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

# IESRequestTunerEvent::GetPriority


## -description



      Gets a code that indicates the priority of a device request for exclusive access to a tuner and its Conditional Access Services (CAS).


## -parameters




### -param pbyPriority [out, retval]

Gets a 1-byte code that indicates the priority. The code can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x00</b></dt>
</dl>
</td>
<td width="60%">
OPPORTUNISTIC.  The device that receives the request should see if the request conflicts with any other tuner usage, including scheduled and live viewing usages.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x01</b></dt>
</dl>
</td>
<td width="60%">
NOTIFY.  The device that receives the request should check to see if the request conflicts with any other scheduled usage.  If the acquisition conflicts with live viewing, the device should prompt the user before relinquishing access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0x02-0xFE</b></dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0xFF</b></dt>
</dl>
</td>
<td width="60%">
IMMEDIATE.  The device that receives the request must release the tuner for the requestor ownership within the next 60 seconds.   The requestor can forcibly acquire the tuner after 60 seconds. 

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da1183a3-6f31-402a-b103-448cf13705a9">IESRequestTunerEvent</a>
 

 

