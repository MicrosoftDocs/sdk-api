---
UID: NF:wia_xp.LPSAFEARRAY_UserMarshal
title: LPSAFEARRAY_UserMarshal function
author: windows-sdk-content
description: Marshals data from the specified SAFEARRAY object to the user's RPC buffer on the client or server side.
old-location: automat\lpsafearray_usermarshal.htm
tech.root: automat
ms.assetid: 8255d1a0-b102-443d-a10f-8c6bd9047703
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LPSAFEARRAY_UserMarshal, LPSAFEARRAY_UserMarshal function [Automation], _oa96_LPSAFEARRAY_UserMarshal, automat.lpsafearray_usermarshal, wia_xp/LPSAFEARRAY_UserMarshal
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - LPSAFEARRAY_UserMarshal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPSAFEARRAY_UserMarshal function


## -description


Marshals data from the specified <a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> object to the user's RPC buffer on the client or server side. 


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD




#### - [in]

The data used by RPC.


#### - pBuffer [in, out]

The current buffer. This pointer may or may not be aligned on entry. The function aligns the buffer pointer, marshals the data, and returns the new buffer position, which is the address of the first byte after the marshaled object.


#### - ppSafeArray [in]

The safe array that contains the data to marshal.


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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppSafeArray</i> parameter is not a valid safe array.


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
The array could not be locked.

</td>
</tr>
</table>
 



