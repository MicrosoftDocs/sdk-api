---
UID: NF:tapi3if.ITCallInfo.get_CallInfoString
title: ITCallInfo::get_CallInfoString
author: windows-sdk-content
description: The get_CallInfoString method gets call information items described by a string, such as the displayable address.
old-location: tapi3\itcallinfo_get_callinfostring.htm
tech.root: tapi
ms.assetid: 248022e7-c6cf-4c46-be94-ee1b79b9f39a
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallInfoString method, ITCallInfo.get_CallInfoString, ITCallInfo::get_CallInfoString, _tapi3_itcallinfo_get_callinfostring, get_CallInfoString, get_CallInfoString method [TAPI 2.2], get_CallInfoString method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callinfostring, tapi3if/ITCallInfo::get_CallInfoString
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
 - ITCallInfo.get_CallInfoString
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
- ITCallInfo.get_CallInfoString
: 
---

# ITCallInfo::get_CallInfoString


## -description


The 
<b>get_CallInfoString</b> method gets call information items described by a string, such as the displayable address.


## -parameters




### -param CallInfoString [in]


<a href="https://msdn.microsoft.com/28482ba8-c536-48ef-bca6-eba5b801c06e">CALLINFO_STRING</a> indicator of information type needed, such as CIS_DISPLAYABLEADDRESS.


### -param ppCallInfoString [out]

Pointer to <b>BSTR</b> representation of needed string.


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
The <i>ppCallInfoString</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>CallInfoString</i> parameter is not a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The current 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a> is not valid for this operation.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppCallInfoString</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/28482ba8-c536-48ef-bca6-eba5b801c06e">CALLINFO_STRING</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/d22f1afb-e036-40d0-9a7f-61d8d24d2376">put_CallInfoString</a>
 

 

