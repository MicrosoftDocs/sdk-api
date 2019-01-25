---
UID: NF:tapi3if.IEnumBstr.Next
title: IEnumBstr::Next
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.
old-location: tapi3\ienumbstr_next.htm
tech.root: Tapi
ms.assetid: e4a03985-9f90-4ae4-b4ec-a6aa43e5bb10
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumBstr interface [TAPI 2.2],Next method, IEnumBstr.Next, IEnumBstr::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumBstr interface, _tapi3_ienumbstr_next, tapi3.ienumbstr_next, tapi3if/IEnumBstr::Next
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
 - IEnumBstr.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBstr::Next


## -description


The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppStrings [out]

Pointer to the list of <b>BSTR</b> pointers returned.


### -param pceltFetched [in, out]

Pointer to number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.


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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppStrings</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppStrings</i> parameter.



