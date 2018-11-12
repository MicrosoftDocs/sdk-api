---
UID: NF:tapi3if.ITSubStream.SelectTerminal
title: ITSubStream::SelectTerminal
author: windows-sdk-content
description: The SelectTerminal method selects an ITTerminal object onto the substream. See the Remarks section under ITStream::SelectTerminal for additional information.
old-location: tapi3\itsubstream_selectterminal.htm
tech.root: tapi
ms.assetid: 5dc558ab-7422-4106-831e-9d2812530e0a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITSubStream interface [TAPI 2.2],SelectTerminal method, ITSubStream.SelectTerminal, ITSubStream::SelectTerminal, SelectTerminal, SelectTerminal method [TAPI 2.2], SelectTerminal method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_selectterminal, tapi3.itsubstream_selectterminal, tapi3if/ITSubStream::SelectTerminal
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
 - ITSubStream.SelectTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStream::SelectTerminal


## -description


The 
<b>SelectTerminal</b> method selects an 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> object onto the substream. See the Remarks section under 
<a href="https://msdn.microsoft.com/ecc4c7eb-c278-457a-b54e-5f1e582e22bf">ITStream::SelectTerminal</a> for additional information.


## -parameters




### -param pTerminal [in]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface of selected terminal.


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
The <i>pTerminal</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_MAXTERMINALS</b></dt>
</dl>
</td>
<td width="60%">
Multiple terminals have been selected on the substream, but media mixing or splitting is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALIDTERMINAL</b></dt>
</dl>
</td>
<td width="60%">
The terminal selected is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ecc4c7eb-c278-457a-b54e-5f1e582e22bf">ITStream::SelectTerminal</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

