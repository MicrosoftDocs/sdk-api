---
UID: NF:recapis.GetLatticePtr
title: GetLatticePtr function
author: windows-sdk-content
description: Retrieves a pointer to the lattice for the current results.
old-location: tablet\getlatticeptr.htm
old-project: tablet
ms.assetid: 5c483500-c58f-4fd0-903a-a3011727bab8
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 5c483500-c58f-4fd0-903a-a3011727bab8, GetLatticePtr, GetLatticePtr function [Tablet PC], recapis/GetLatticePtr, tablet.getlatticeptr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: recapis.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
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
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetLatticePtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# GetLatticePtr function


## -description



Retrieves a pointer to the lattice for the current results.




## -parameters




### -param hrc

The handle to the recognizer context.


### -param ppLattice

The recognition results.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The recognizer does not support this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_NOT_RELEVANT</b></dt>
</dl>
</td>
<td width="60%">
The recognizer context does not contain results.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was received.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/628ca677-31eb-47d9-bcc6-d7777f8aaf7c">Recognizer Lattice Structure</a>
 

 

