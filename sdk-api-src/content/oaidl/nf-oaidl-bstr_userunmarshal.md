---
UID: NF:oaidl.BSTR_UserUnmarshal
title: BSTR_UserUnmarshal function (oaidl.h)
description: Unmarshals a BSTR object from the RPC buffer.
old-location: automat\bstr_userunmarshal.htm
tech.root: automat
ms.assetid: d0a6229e-7091-4859-b539-d1e29044171a
ms.date: 12/05/2018
ms.keywords: BSTR_UserUnmarshal, BSTR_UserUnmarshal function [Automation], _oa96_BSTR_UserUnmarshal, automat.bstr_userunmarshal, oaidl/BSTR_UserUnmarshal
f1_keywords:
- oaidl/BSTR_UserUnmarshal
dev_langs:
- c++
req.header: oaidl.h
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
- BSTR_UserUnmarshal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BSTR_UserUnmarshal function


## -description


Unmarshals a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/bstr">BSTR</a> object from the RPC buffer.


## -parameters




### -param arg1 [in]

The data used by RPC.


### -param arg2 [in]

The current buffer. This pointer may or may not be aligned on entry.


### -param arg3 [out]

The object.


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
Insufficient memory for this function to perform.

</td>
</tr>
</table>
 



