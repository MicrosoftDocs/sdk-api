---
UID: NF:wia_xp.LPSAFEARRAY_UserUnmarshal64
title: LPSAFEARRAY_UserUnmarshal64 function
author: windows-sdk-content
description: Unmarshals a SAFEARRAY object from the RPC buffer.
old-location: automat\lpsafearray_userunmarshal64.htm
old-project: automat
ms.assetid: 19B52C54-0905-446C-A8D9-C98153931708
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: LPSAFEARRAY_UserUnmarshal64, LPSAFEARRAY_UserUnmarshal64 function [Automation], automat.lpsafearray_userunmarshal64, wia_xp/LPSAFEARRAY_UserUnmarshal64
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wia_xp.h
req.include-header: Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	LPSAFEARRAY_UserUnmarshal64
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# LPSAFEARRAY_UserUnmarshal64 function


## -description


Unmarshals a <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> object from the RPC buffer.


## -parameters




### -param

TBD




#### - pBuffer [in, out]

The current buffer. This pointer may or may not be aligned on entry. The function aligns the buffer pointer, marshals the data, and returns the new buffer position, which is the address of the first byte after the marshaled object.


#### - pFlags [in]

The data used by RPC.


#### - ppSafeArray [in]

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
The <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> object does not have the correct dimensions, does not have the correct features, or memory cannot be reallocated.

</td>
</tr>
</table>
 



