---
UID: NF:tapi3if.ITAddress.get_MessageWaiting
title: ITAddress::get_MessageWaiting
author: windows-sdk-content
description: The get_MessageWaiting method determines if the address has a message waiting.
old-location: tapi3\itaddress_get_messagewaiting.htm
old-project: Tapi
ms.assetid: 4ddb49d9-dde7-498b-a243-f8c5b1294a87
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_MessageWaiting method, ITAddress.get_MessageWaiting, ITAddress::get_MessageWaiting, _tapi3_itaddress_get_messagewaiting, get_MessageWaiting, get_MessageWaiting method [TAPI 2.2], get_MessageWaiting method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_messagewaiting, tapi3if/ITAddress::get_MessageWaiting
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAddress.get_MessageWaiting
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddress::get_MessageWaiting


## -description


The 
<b>get_MessageWaiting</b> method determines if the address has a message waiting.


## -parameters




### -param pfMessageWaiting [out]

If VARIANT_TRUE is returned, a message is waiting; if VARIANT_FALSE is returned, no message is waiting.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfMessageWaiting</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



In TAPI 2.<i>x</i>, this maps to the flag LINEDEVSTATUSFLAGS_MSGWAIT being set or not in the member <i>dwDevStatusFlags</i> from the structure 
<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/3d565e99-eb90-47ca-9fb9-295236f566fb">LINEDEVSTATUS</a>



<a href="https://msdn.microsoft.com/9dc125ab-a452-4108-93d5-9f341b879e8d">put_MessageWaiting</a>
 

 

