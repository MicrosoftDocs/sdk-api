---
UID: NF:oaidl.VARIANT_UserUnmarshal64
title: VARIANT_UserUnmarshal64 function
author: windows-sdk-content
description: Unmarshals a VARIANT object from the RPC buffer.
old-location: automat\variant_userunmarshal64.htm
old-project: automat
ms.assetid: c4539285-20c2-4eda-acbc-1f1a80cad07b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VARIANT_UserUnmarshal64, VARIANT_UserUnmarshal64 function [Automation], automat.variant_userunmarshal64, oaidl/VARIANT_UserUnmarshal64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VARIANT_UserUnmarshal64
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# VARIANT_UserUnmarshal64 function


## -description


Unmarshals a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> object from the RPC buffer.


## -parameters




### -param

TBD




#### - [in]

The data used by RPC.


#### - pBuffer [in]

The current buffer. This pointer may or may not be aligned on entry.


#### - pVariant [out]

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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not valid.

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
The stub data for the buffer size is incorrect.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE
</b></dt>
</dl>
</td>
<td width="60%">
The input parameter is not a valid type of variant.


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
 



