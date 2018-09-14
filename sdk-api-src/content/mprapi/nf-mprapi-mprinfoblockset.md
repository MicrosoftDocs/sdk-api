---
UID: NF:mprapi.MprInfoBlockSet
title: MprInfoBlockSet function
author: windows-sdk-content
description: The MprInfoBlockSet creates a new header that is identical to an existing header with a specified block modified.
old-location: rras\mprinfoblockset.htm
tech.root: rras
ms.assetid: 55912927-d886-46d1-a5c1-e10f19c117ab
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: MprInfoBlockSet, MprInfoBlockSet function [RAS], _mpr_mprinfoblockset, mprapi/MprInfoBlockSet, rras.mprinfoblockset
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprInfoBlockSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprInfoBlockSet function


## -description


The 
<b>MprInfoBlockSet</b> creates a new header that is identical to an existing header with a specified block modified.


## -parameters




### -param lpHeader [in]

Pointer to the header in which to modify the specified block.


### -param dwInfoType [in]

Specifies the type of block to change. The types available depend on the transport: 
<a href="https://msdn.microsoft.com/911c61d4-e500-48c6-8861-39dbc09ab4e7">IP</a> or 
<a href="https://msdn.microsoft.com/6cbc8415-f5ba-4f84-a23f-dd4f4a54d118">IPX</a>.


### -param dwItemSize [in]

Specifies the size of each item in the block's new data.


### -param dwItemCount [in]

Specifies the number of items of size <i>dwItemSize</i> to be copied as the new data for the block.


### -param lpItemData [in]

Pointer to the new data for the block. This should point to a buffer with a size (in bytes) equal to the product of <i>dwItemSize</i> and <i>dwItemCount</i>.


### -param lplpNewHeader [out]

Pointer to a pointer variable that, on successful return, points to the new header.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following values.

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
One (or more) required parameters is <b>NULL</b>, or no block of type <i>dwInfoType</i> exists in the header.

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
 




## -see-also




<a href="_win32_formatmessage">FormatMessage</a>



<a href="https://msdn.microsoft.com/389002c9-2d24-4b35-ab5b-801fe2091db9">MprInfo Functions and Information Headers</a>



<a href="https://msdn.microsoft.com/94d8fc3b-1ed6-4555-85c0-40e32d197a72">MprInfoBlockAdd</a>



<a href="https://msdn.microsoft.com/2d124541-c954-4031-95cd-68a96c8e0a77">MprInfoBlockRemove</a>
 

 

