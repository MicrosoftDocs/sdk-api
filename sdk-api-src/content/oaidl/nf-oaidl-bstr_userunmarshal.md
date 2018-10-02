---
UID: NF:oaidl.BSTR_UserUnmarshal
title: BSTR_UserUnmarshal function
author: windows-sdk-content
description: Unmarshals a BSTR object from the RPC buffer.
old-location: automat\bstr_userunmarshal.htm
tech.root: automat
ms.assetid: d0a6229e-7091-4859-b539-d1e29044171a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BSTR_UserUnmarshal, BSTR_UserUnmarshal function [Automation], _oa96_BSTR_UserUnmarshal, automat.bstr_userunmarshal, oaidl/BSTR_UserUnmarshal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BSTR_UserUnmarshal function


## -description


Unmarshals a <a href="https://msdn.microsoft.com/1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> object from the RPC buffer.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD




#### - [in]

The data used by RPC.


#### - pBstr [out]

The object.


#### - pBuffer [in]

The current buffer. This pointer may or may not be aligned on entry.


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
 



