---
UID: NF:oaidl.BSTR_UserUnmarshal64
title: BSTR_UserUnmarshal64 function (oaidl.h)
description: Unmarshals a BSTR object from the RPC buffer. (BSTR_UserUnmarshal64)
helpviewer_keywords: ["BSTR_UserUnmarshal64","BSTR_UserUnmarshal64 function [Automation]","automat.bstr_userunmarshal64","oaidl/BSTR_UserUnmarshal64"]
old-location: automat\bstr_userunmarshal64.htm
tech.root: automat
ms.assetid: 5d0bb71f-f8a2-4af7-b7e4-177997af2c9b
ms.date: 12/05/2018
ms.keywords: BSTR_UserUnmarshal64, BSTR_UserUnmarshal64 function [Automation], automat.bstr_userunmarshal64, oaidl/BSTR_UserUnmarshal64
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BSTR_UserUnmarshal64
 - oaidl/BSTR_UserUnmarshal64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - BSTR_UserUnmarshal64
---

# BSTR_UserUnmarshal64 function


## -description

Unmarshals a <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> object from the RPC buffer.

## -parameters

### -param unnamedParam1 [in]

The data used by RPC.

### -param unnamedParam2 [in]

The current buffer. This pointer may or may not be aligned on entry.

### -param unnamedParam3 [out]

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
