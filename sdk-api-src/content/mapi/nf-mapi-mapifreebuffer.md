---
UID: NF:mapi.MAPIFreeBuffer
title: MAPIFreeBuffer function
author: windows-sdk-content
description: The MAPIFreeBuffer function frees memory allocated by the messaging system.
old-location: mapi\mapifreebuffer.htm
old-project: WindowsMAPI
ms.assetid: b67a2a42-edba-4372-b3b7-5bf3e9d3e5ed
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: MAPIFreeBuffer, MAPIFreeBuffer function, mapi.mapifreebuffer, wabmem/MAPIFreeBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mapi.h
req.include-header: Mapi.h
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
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mapi32.dll
api_name:
-	MAPIFreeBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: Mapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# MAPIFreeBuffer function


## -description


<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIFreeBuffer</b> function frees memory allocated by the messaging system.


## -parameters




### -param pv [in]

Pointer to memory allocated by the messaging system. This pointer is returned by the <a href="https://msdn.microsoft.com/46a8ff9f-17d9-4c33-8ca4-0a3978013f52">MAPIReadMail</a>, <a href="https://msdn.microsoft.com/4f01763d-22a2-4ee4-a559-f875cb06ea6b">MAPIAddress</a>, and <a href="https://msdn.microsoft.com/c834ea40-62c6-44a8-b0e1-f569a92b4c83">MAPIResolveName</a> functions.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred. The memory could not be freed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the memory was freed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d04316cf-31f5-4f5f-ad20-01ce720fdf4c">MAPILogoff</a>



<a href="https://msdn.microsoft.com/a8330f38-3ef0-4b36-a5e7-89837088cbef">Simple MAPI</a>
 

 

