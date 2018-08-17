---
UID: NF:tapi3if.ITCallInfo.put_CallInfoString
title: ITCallInfo::put_CallInfoString
author: windows-sdk-content
description: The put_CallInfoString method sets call information items described by a string, such as the displayable address.
old-location: tapi3\itcallinfo_put_callinfostring.htm
old-project: tapi
ms.assetid: d22f1afb-e036-40d0-9a7f-61d8d24d2376
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],put_CallInfoString method, ITCallInfo.put_CallInfoString, ITCallInfo::put_CallInfoString, _tapi3_itcallinfo_put_callinfostring, put_CallInfoString, put_CallInfoString method [TAPI 2.2], put_CallInfoString method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_put_callinfostring, tapi3if/ITCallInfo::put_CallInfoString
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
 - Tapi3.dll
api_name:
 - ITCallInfo.put_CallInfoString
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallInfo::put_CallInfoString


## -description


The 
<b>put_CallInfoString</b> method sets call information items described by a string, such as the displayable address.


## -parameters




### -param CallInfoString [in]


<a href="https://msdn.microsoft.com/28482ba8-c536-48ef-bca6-eba5b801c06e">CALLINFO_STRING</a> indicator of information type, such as CIS_DISPLAYABLEADDRESS.


### -param pCallInfoString [in]

Pointer to a BSTR representation of the string.


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
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the string data referenced by <i>pCallInfoString</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/28482ba8-c536-48ef-bca6-eba5b801c06e">CALLINFO_STRING</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/248022e7-c6cf-4c46-be94-ee1b79b9f39a">get_CallInfoString</a>
 

 

