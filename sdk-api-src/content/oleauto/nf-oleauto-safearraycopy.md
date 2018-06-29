---
UID: NF:oleauto.SafeArrayCopy
title: SafeArrayCopy function
author: windows-sdk-content
description: Creates a copy of an existing safe array.
old-location: automat\safearraycopy.htm
old-project: automat
ms.assetid: 8f84d4f6-1852-4ad8-b174-f3fa37e5bbd6
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SafeArrayCopy, SafeArrayCopy function [Automation], _oa96_SafeArrayCopy, automat.safearraycopy, oleauto/SafeArrayCopy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
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
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayCopy
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# SafeArrayCopy function


## -description


Creates a copy of an existing safe array.


## -parameters




### -param psa [in]

A safe array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.



### -param ppsaOut [out]

The safe array descriptor.


## -returns



This function can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



<b>SafeArrayCopy</b> calls the string or variant manipulation functions if the array to copy contains either of these data types. If the array being copied contains object references, the reference counts for the objects are incremented.




## -see-also




<a href="https://msdn.microsoft.com/f98bff39-bc5f-4a81-85d7-d5228e20fbc8">SysAllocStringLen</a>



<a href="https://msdn.microsoft.com/f6ddbe1f-37b0-44f1-a3f0-b7ef4df88f8a">VariantCopy</a>



<a href="https://msdn.microsoft.com/5d9be6cd-92e5-485c-ba0d-8630d3e414b8">VariantCopyInd</a>
 

 

