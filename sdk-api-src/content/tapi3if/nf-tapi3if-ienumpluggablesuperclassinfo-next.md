---
UID: NF:tapi3if.IEnumPluggableSuperclassInfo.Next
title: IEnumPluggableSuperclassInfo::Next
author: windows-sdk-content
description: The Next method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.
old-location: tapi3\ienumpluggablesuperclassinfo_next.htm
old-project: Tapi
ms.assetid: 820cf2cd-1354-473d-974d-267b888f07a9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IEnumPluggableSuperclassInfo interface [TAPI 2.2],Next method, IEnumPluggableSuperclassInfo.Next, IEnumPluggableSuperclassInfo::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumPluggableSuperclassInfo interface, _tapi3_ienumpluggablesuperclassinfo_next, tapi3.ienumpluggablesuperclassinfo_next, tapi3if/IEnumPluggableSuperclassInfo::Next
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumPluggableSuperclassInfo.Next
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumPluggableSuperclassInfo::Next


## -description


The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.


## -parameters




### -param celt [in]

Number of elements requested.


### -param ppElements [out]

Pointer to 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> list of pointers returned.


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
The <i>ppElements</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a> interface returned by <b>IEnumPluggableSuperclassInfo::Next</b>. The application must call <a href="_com_iunknown_release">Release</a> on the <a href="https://msdn.microsoft.com/80b84976-4256-47d2-a965-3ebe89a3821a">IEnumPluggableSuperclassInfo</a> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/80b84976-4256-47d2-a965-3ebe89a3821a">IEnumPluggableSuperclassInfo</a>



<a href="https://msdn.microsoft.com/f9226af1-90e7-4317-af73-e1563883e2b6">ITPluggableTerminalSuperclassInfo</a>
 

 

