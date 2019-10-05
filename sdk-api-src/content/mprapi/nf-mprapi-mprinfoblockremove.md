---
UID: NF:mprapi.MprInfoBlockRemove
title: MprInfoBlockRemove function (mprapi.h)
author: windows-sdk-content
description: The MprInfoBlockRemove function creates a new header that is identical to an existing header with a specified block removed.
old-location: rras\mprinfoblockremove.htm
tech.root: RRAS
ms.assetid: 2d124541-c954-4031-95cd-68a96c8e0a77
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprInfoBlockRemove, MprInfoBlockRemove function [RAS], _mpr_mprinfoblockremove, mprapi/MprInfoBlockRemove, rras.mprinfoblockremove
ms.topic: function
f1_keywords: 
 - "mprapi/MprInfoBlockRemove"
dev_langs:
 - c++
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
 - MprInfoBlockRemove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprInfoBlockRemove function


## -description


The 
<b>MprInfoBlockRemove</b> function creates a new header that is identical to an existing header with a specified block removed.


## -parameters




### -param lpHeader [in]

Pointer to the header from which the block should be removed.


### -param dwInfoType [in]

Specifies the type of block to be removed. The types available depend on the transport: 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/ip-information-types-for-router-information-blocks">IP</a> or 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/ipx-information-types-for-router-information-blocks">IPX</a>.


### -param lplpNewHeader [out]

Pointer to a pointer variable that receives the new header.


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
The <i>lpHeader</i> parameter is <b>NULL</b>, or no block of type <i>dwInfoType</i> exists in the header.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The memory allocation required for successful execution of 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a> could not be completed.

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
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>
 




## -remarks



After removing an information block, obtain the new size of the information header by call 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockquerysize">MprInfoBlockQuerySize</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockadd">MprInfoBlockAdd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockquerysize">MprInfoBlockQuerySize</a>
 

 

