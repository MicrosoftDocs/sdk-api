---
UID: NF:tapi3if.ITSubStreamControl.CreateSubStream
title: ITSubStreamControl::CreateSubStream
author: windows-sdk-content
description: The CreateSubStream method creates a substream.
old-location: tapi3\itsubstreamcontrol_createsubstream.htm
tech.root: TAPI
ms.assetid: 00fe0f8f-c814-4ae6-a60b-c58f3dc60b67
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateSubStream, CreateSubStream method [TAPI 2.2], CreateSubStream method [TAPI 2.2],ITSubStreamControl interface, ITSubStreamControl interface [TAPI 2.2],CreateSubStream method, ITSubStreamControl.CreateSubStream, ITSubStreamControl::CreateSubStream, _tapi3_itsubstreamcontrol_createsubstream, tapi3.itsubstreamcontrol_createsubstream, tapi3if/ITSubStreamControl::CreateSubStream
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITSubStreamControl.CreateSubStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStreamControl::CreateSubStream


## -description


The 
<b>CreateSubStream</b> method creates a substream.


## -parameters




### -param ppSubStream [out]

Pointer to 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> interface created.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppSubStream</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_MAXSTREAMS</b></dt>
</dl>
</td>
<td width="60%">
Substream cannot be created because the maximum number of streams has already been reached.

</td>
</tr>
</table>
 




## -remarks



Many MSPs do not support dynamic creation of substreams, and simply return TAPI_E_MAXSTREAMS in their implementation of this method.

TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> interface returned by <b>ITSubStreamControl::CreateSubStream</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<b>ITSubStream</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

