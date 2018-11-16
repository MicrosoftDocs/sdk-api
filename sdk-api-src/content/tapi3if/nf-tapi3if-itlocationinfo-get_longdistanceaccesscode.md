---
UID: NF:tapi3if.ITLocationInfo.get_LongDistanceAccessCode
title: ITLocationInfo::get_LongDistanceAccessCode
author: windows-sdk-content
description: The get_LongDistanceAccessCode method gets the code to access long distance.
old-location: tapi3\itlocationinfo_get_longdistanceaccesscode.htm
tech.root: Tapi
ms.assetid: c35e6a6a-3740-4595-90cd-709b4c9a42d1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_LongDistanceAccessCode method, ITLocationInfo.get_LongDistanceAccessCode, ITLocationInfo::get_LongDistanceAccessCode, _tapi3_itlocationinfo_get_longdistanceaccesscode, get_LongDistanceAccessCode, get_LongDistanceAccessCode method [TAPI 2.2], get_LongDistanceAccessCode method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_longdistanceaccesscode, tapi3if/ITLocationInfo::get_LongDistanceAccessCode
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLocationInfo.get_LongDistanceAccessCode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITLocationInfo.get_LongDistanceAccessCode
: 
---

# ITLocationInfo::get_LongDistanceAccessCode


## -description


The 
<b>get_LongDistanceAccessCode</b> method gets the code to access long distance.


## -parameters




### -param ppCode [out]

Pointer to <b>BSTR</b> representation of long distance access code.


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
The <i>ppCode</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCode</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppCode</i> parameter.
			

The value that this method returns corresponds to the <b>dwLongDistanceAccessCodeSize</b> and <b>dwLongDistanceAccessCodeOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

