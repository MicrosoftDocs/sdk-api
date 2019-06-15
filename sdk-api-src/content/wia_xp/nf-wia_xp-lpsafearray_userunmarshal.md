---
UID: NF:wia_xp.LPSAFEARRAY_UserUnmarshal
title: LPSAFEARRAY_UserUnmarshal function (wia_xp.h)
author: windows-sdk-content
description: Unmarshals a SAFEARRAY object from the RPC buffer.
old-location: automat\lpsafearray_userunmarshal.htm
tech.root: automat
ms.assetid: 8798b8c1-d1c0-4729-b7bd-0329e8b71b0d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LPSAFEARRAY_UserUnmarshal, LPSAFEARRAY_UserUnmarshal function [Automation], _oa96_LPSAFEARRAY_UserUnmarshal, automat.lpsafearray_userunmarshal, wia_xp/LPSAFEARRAY_UserUnmarshal
ms.topic: function
req.header: wia_xp.h
req.include-header: Propidlbase.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - LPSAFEARRAY_UserUnmarshal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPSAFEARRAY_UserUnmarshal function


## -description


Unmarshals a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ns-oaidl-tagsafearray">SAFEARRAY</a> object from the RPC buffer.


## -parameters




### -param arg1 [in]

The data used by RPC.


### -param arg2 [in, out]

The current buffer. This pointer may or may not be aligned on entry. The function aligns the buffer pointer, marshals the data, and returns the new buffer position, which is the address of the first byte after the marshaled object.


### -param arg3 [in]

Receives the safe array that contains the data.


## -returns



The value obtained from the returned <b>HRESULT</b> value is one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_BAD_STUB_DATA
</b></dt>
</dl>
</td>
<td width="60%">
The stub has received bad data.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED
</b></dt>
</dl>
</td>
<td width="60%">
The array could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for this function to perform.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADCALLEE
</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ns-oaidl-tagsafearray">SAFEARRAY</a> object does not have the correct dimensions, does not have the correct features, or memory cannot be reallocated.

</td>
</tr>
</table>
 



