---
UID: NF:recapis.GetLatticePtr
title: GetLatticePtr function (recapis.h)
description: Retrieves a pointer to the lattice for the current results.
helpviewer_keywords: ["5c483500-c58f-4fd0-903a-a3011727bab8","GetLatticePtr","GetLatticePtr function [Tablet PC]","recapis/GetLatticePtr","tablet.getlatticeptr"]
old-location: tablet\getlatticeptr.htm
tech.root: tablet
ms.assetid: 5c483500-c58f-4fd0-903a-a3011727bab8
ms.date: 11/06/2024
ms.keywords: 5c483500-c58f-4fd0-903a-a3011727bab8, GetLatticePtr, GetLatticePtr function [Tablet PC], recapis/GetLatticePtr, tablet.getlatticeptr
req.header: recapis.h
req.include-header: 
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
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetLatticePtr
 - recapis/GetLatticePtr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport 
api_location:
 - recapis.h
 - inkobjcore.dll
 - mshwgst.dll
api_name:
 - GetLatticePtr
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

<a href="/windows/desktop/tablet/recognizer-lattice-structure">Recognizer Lattice Structure</a>