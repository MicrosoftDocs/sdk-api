---
UID: NF:tapi3if.ITAddress.put_MessageWaiting
title: ITAddress::put_MessageWaiting
author: windows-sdk-content
description: The put_MessageWaiting method sets the status of the message waiting on the address.
old-location: tapi3\itaddress_put_messagewaiting.htm
old-project: tapi
ms.assetid: 9dc125ab-a452-4108-93d5-9f341b879e8d
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAddress interface [TAPI 2.2],put_MessageWaiting method, ITAddress.put_MessageWaiting, ITAddress::put_MessageWaiting, _tapi3_itaddress_put_messagewaiting, put_MessageWaiting, put_MessageWaiting method [TAPI 2.2], put_MessageWaiting method [TAPI 2.2],ITAddress interface, tapi3.itaddress_put_messagewaiting, tapi3if/ITAddress::put_MessageWaiting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress.put_MessageWaiting
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddress::put_MessageWaiting


## -description


The 
<b>put_MessageWaiting</b> method sets the status of the message waiting on the address.


## -parameters




### -param fMessageWaiting [in]

Status of message waiting to be set.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>fMessageWaiting</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>
 




## -remarks



For programmers familiar with TAPI 2.<i>x:</i> This method turns on and off the flag LINEDEVSTATUSFLAGS_MSGWAIT in the <b>dwDevStatusFlags</b> member of the 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a> structure by calling 
<a href="https://msdn.microsoft.com/c8eb142d-5160-49f3-81c1-61094c180df8">lineSetLineDevStatus</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a>



<a href="https://msdn.microsoft.com/4ddb49d9-dde7-498b-a243-f8c5b1294a87">get_MessageWaiting</a>



<a href="https://msdn.microsoft.com/c8eb142d-5160-49f3-81c1-61094c180df8">lineSetLineDevStatus</a>
 

 

