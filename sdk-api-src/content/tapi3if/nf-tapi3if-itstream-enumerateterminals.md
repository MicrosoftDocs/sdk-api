---
UID: NF:tapi3if.ITStream.EnumerateTerminals
title: ITStream::EnumerateTerminals
author: windows-sdk-content
description: The EnumerateTerminals method enumerates terminals selected on the stream. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the get_Terminals method.
old-location: tapi3\itstream_enumerateterminals.htm
tech.root: tapi
ms.assetid: c57af2a9-a2ec-45ba-9e10-7b5f41bdeb00
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumerateTerminals, EnumerateTerminals method [TAPI 2.2], EnumerateTerminals method [TAPI 2.2],ITStream interface, ITStream interface [TAPI 2.2],EnumerateTerminals method, ITStream.EnumerateTerminals, ITStream::EnumerateTerminals, _tapi3_itstream_enumerateterminals, tapi3.itstream_enumerateterminals, tapi3if/ITStream::EnumerateTerminals
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
 - ITStream.EnumerateTerminals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStream::EnumerateTerminals


## -description


The 
<b>EnumerateTerminals</b> method enumerates terminals selected on the stream. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the 
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



TAPI calls the <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a> interface returned by <b>ITStream::EnumerateTerminals</b>. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a364e466-1d10-402f-935d-ff2713522fed">IEnumTerminal</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

