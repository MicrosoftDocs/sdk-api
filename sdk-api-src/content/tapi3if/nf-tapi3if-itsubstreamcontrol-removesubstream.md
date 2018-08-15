---
UID: NF:tapi3if.ITSubStreamControl.RemoveSubStream
title: ITSubStreamControl::RemoveSubStream
author: windows-sdk-content
description: The RemoveSubStream method removes a substream.
old-location: tapi3\itsubstreamcontrol_removesubstream.htm
old-project: tapi
ms.assetid: 1a1be17c-2cae-4eea-a20a-3344915c5234
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITSubStreamControl interface [TAPI 2.2],RemoveSubStream method, ITSubStreamControl.RemoveSubStream, ITSubStreamControl::RemoveSubStream, RemoveSubStream, RemoveSubStream method [TAPI 2.2], RemoveSubStream method [TAPI 2.2],ITSubStreamControl interface, _tapi3_itsubstreamcontrol_removesubstream, tapi3.itsubstreamcontrol_removesubstream, tapi3if/ITSubStreamControl::RemoveSubStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
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
 - tapi3if.h
api_name:
 - ITSubStreamControl.RemoveSubStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSubStreamControl::RemoveSubStream


## -description


The 
<b>RemoveSubStream</b> method removes a substream.


## -parameters




### -param pSubStream [in]

Pointer to 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> to be removed.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>pSubStream</i> parameter does not point to a valid interface.

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
<dt><b>TAPI_E_INVALIDSTREAM</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSubStream</i> parameter does not point to a valid substream.

</td>
</tr>
</table>
 




## -remarks



Some MSPs may not support the advanced concept of creating and removing substreams, and simply return TAPI_E_NOTSUPPORTED.




## -see-also




<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

