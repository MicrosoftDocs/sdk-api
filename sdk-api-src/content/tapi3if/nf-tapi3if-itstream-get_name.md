---
UID: NF:tapi3if.ITStream.get_Name
title: ITStream::get_Name
author: windows-sdk-content
description: The get_Name method gets a BSTR representing the name of the stream. This name is used for informational or display purposes.
old-location: tapi3\itstream_get_name.htm
tech.root: tapi
ms.assetid: b3b81bd7-f99a-4cb1-8d60-6be8c1e68722
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITStream interface [TAPI 2.2],get_Name method, ITStream.get_Name, ITStream::get_Name, _tapi3_itstream_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITStream interface, tapi3.itstream_get_name, tapi3if/ITStream::get_Name
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
 - ITStream.get_Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStream::get_Name


## -description


The 
<b>get_Name</b> method gets a <b>BSTR</b> representing the name of the stream. This name is used for informational or display purposes.


## -parameters




### -param ppName [out]

Pointer to <b>BSTR</b> representation of stream's name.


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
The <i>ppName</i> parameter is not a valid pointer.

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



The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

