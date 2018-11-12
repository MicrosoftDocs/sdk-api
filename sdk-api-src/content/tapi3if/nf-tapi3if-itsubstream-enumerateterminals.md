---
UID: NF:tapi3if.ITSubStream.EnumerateTerminals
title: ITSubStream::EnumerateTerminals
author: windows-sdk-content
description: The EnumerateTerminals method enumerates terminals selected on the substream. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the get_Terminals method.
old-location: tapi3\itsubstream_enumerateterminals.htm
tech.root: tapi
ms.assetid: bf5e1f7f-3820-433e-b71f-53798c202593
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: EnumerateTerminals, EnumerateTerminals method [TAPI 2.2], EnumerateTerminals method [TAPI 2.2],ITSubStream interface, ITSubStream interface [TAPI 2.2],EnumerateTerminals method, ITSubStream.EnumerateTerminals, ITSubStream::EnumerateTerminals, _tapi3_itsubstream_enumerateterminals, tapi3.itsubstream_enumerateterminals, tapi3if/ITSubStream::EnumerateTerminals
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
 - ITSubStream.EnumerateTerminals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStream::EnumerateTerminals


## -description


The 
<b>EnumerateTerminals</b> method enumerates terminals selected on the substream. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the 
<a href="https://msdn.microsoft.com/2861dbf7-fc13-4182-90e5-32347f3d1e54">get_Terminals</a> method.


## -parameters




### -param ppEnumTerminal [out]

Pointer to an 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> terminal enumerator.


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
The <i>ppEnumTerminal</i> parameter is not a valid pointer.

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
</table>
 




## -remarks



This method returns only the terminals selected on the substream. Other terminals may be selected on the stream or on other substreams within the stream; those terminals are not returned.

TAPI calls the <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> interface returned by <b>ITSubStream::EnumerateTerminals</b>. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

