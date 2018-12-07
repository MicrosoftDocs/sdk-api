---
UID: NF:mprapi.MprInfoBlockAdd
title: MprInfoBlockAdd function
author: windows-sdk-content
description: The MprInfoBlockAdd function creates a new header that is identical to an existing header with the addition of a new block.
old-location: rras\mprinfoblockadd.htm
tech.root: rras
ms.assetid: 94d8fc3b-1ed6-4555-85c0-40e32d197a72
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprInfoBlockAdd, MprInfoBlockAdd function [RAS], _mpr_mprinfoblockadd, mprapi/MprInfoBlockAdd, rras.mprinfoblockadd
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
 - MprInfoBlockAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprInfoBlockAdd function


## -description


The 
<b>MprInfoBlockAdd</b> function creates a new header that is identical to an existing header with the addition of a new block.


## -parameters




### -param lpHeader [in]

Pointer to the header in which to add the new block.


### -param dwInfoType [in]

Specifies the type of block to add. The types available depend on the transport: 
<a href="https://msdn.microsoft.com/911c61d4-e500-48c6-8861-39dbc09ab4e7">IPv4</a>, <a href="https://msdn.microsoft.com/58fa59e6-e0f3-4f04-9c57-585f1d496b31">IPv6</a>, or <a href="https://msdn.microsoft.com/6cbc8415-f5ba-4f84-a23f-dd4f4a54d118">IPX</a>.

<b>Windows Server 2008:  </b>If <i>dwInfoTYpe</i> contains <a href="https://msdn.microsoft.com/911c61d4-e500-48c6-8861-39dbc09ab4e7">IP_ROUTE_INFO</a>, <i>lpItemData</i> must point to a <a href="https://msdn.microsoft.com/6dbf86b8-80bd-4000-8047-91a76875829f">INTERFACE_ROUTE_INFO</a> structure.


### -param dwItemSize [in]

Specifies the size of each item in the block to be added.


### -param dwItemCount [in]

Specifies the number of items of size <i>dwItemSize</i> to be copied as data for the new block.


### -param lpItemData [in]

Pointer to the data for the new block. The size in bytes of this buffer should be equal to the product of <i>dwItemSize</i> and <i>dwItemCount</i>.


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
The <i>lpHeader</i>, <i>lplpNewHeader</i>, or <i>lpItemData</i> parameter is <b>NULL</b>, or a block of type <i>dwInfoType</i> already exists in the header.

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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 




## -remarks



After adding an information block, obtain the new size of the information header by call 
<a href="https://msdn.microsoft.com/cac491c9-3486-4eba-afe9-9e18f50c0643">MprInfoBlockQuerySize</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/389002c9-2d24-4b35-ab5b-801fe2091db9">MprInfo Functions and Information Headers</a>



<a href="https://msdn.microsoft.com/cac491c9-3486-4eba-afe9-9e18f50c0643">MprInfoBlockQuerySize</a>



<a href="https://msdn.microsoft.com/2d124541-c954-4031-95cd-68a96c8e0a77">MprInfoBlockRemove</a>



<a href="https://msdn.microsoft.com/446e93a0-8de5-4117-94fe-6f167da1acef">MprInfoDuplicate</a>
 

 

