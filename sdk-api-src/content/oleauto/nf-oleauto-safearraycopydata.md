---
UID: NF:oleauto.SafeArrayCopyData
title: SafeArrayCopyData function
author: windows-sdk-content
description: Copies the source array to the specified target array after releasing any resources in the target array.
old-location: automat\safearraycopydata.htm
old-project: automat
ms.assetid: 32c1fc4f-3fe0-490f-b5af-640514a8cecc
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SafeArrayCopyData, SafeArrayCopyData function [Automation], _oa96_SafeArrayCopyData, automat.safearraycopydata, oleauto/SafeArrayCopyData
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
 - SafeArrayCopyData
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# SafeArrayCopyData function


## -description


Copies the source array to the specified target array after releasing any resources in the target array. This is similar to <a href="https://msdn.microsoft.com/library/ms221451(v=VS.85).aspx">SafeArrayCopy</a>, except that the target array has to be set up by the caller. The target is not allocated or reallocated.


## -parameters




### -param psaSource [in]

The safe array to copy.


### -param psaTarget [in]

The target safe array.


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
 



