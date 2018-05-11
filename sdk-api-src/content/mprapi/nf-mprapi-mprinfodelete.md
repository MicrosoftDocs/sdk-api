---
UID: NF:mprapi.MprInfoDelete
title: MprInfoDelete function
author: windows-driver-content
description: The MprInfoDelete function deletes an information header created using MprInfoCreate, or retrieved by MprInfoBlockAdd, MprInfoBlockRemove, or MprInfoBlockSet.
old-location: rras\mprinfodelete.htm
old-project: RRAS
ms.assetid: c81b92c2-a977-40e0-b971-e4e70e1a1371
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MprInfoDelete, MprInfoDelete function [RAS], _mpr_mprinfodelete, mprapi/MprInfoDelete, rras.mprinfodelete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprInfoDelete
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprInfoDelete function


## -description


The 
<b>MprInfoDelete</b> function deletes an information header created using 
<a href="https://msdn.microsoft.com/c48fc24f-8cf6-45c0-8ce1-841896648ba7">MprInfoCreate</a>, or retrieved by 
<a href="https://msdn.microsoft.com/94d8fc3b-1ed6-4555-85c0-40e32d197a72">MprInfoBlockAdd</a>, 
<a href="https://msdn.microsoft.com/2d124541-c954-4031-95cd-68a96c8e0a77">MprInfoBlockRemove</a>, or 
<a href="https://msdn.microsoft.com/55912927-d886-46d1-a5c1-e10f19c117ab">MprInfoBlockSet</a>.


## -parameters




### -param lpHeader [in]

Pointer to the header to be deallocated.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpHeader</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
The call failed. Use 
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="_win32_formatmessage">FormatMessage</a>



<a href="https://msdn.microsoft.com/94d8fc3b-1ed6-4555-85c0-40e32d197a72">MprInfoBlockAdd</a>



<a href="https://msdn.microsoft.com/2d124541-c954-4031-95cd-68a96c8e0a77">MprInfoBlockRemove</a>



<a href="https://msdn.microsoft.com/55912927-d886-46d1-a5c1-e10f19c117ab">MprInfoBlockSet</a>
 

 

