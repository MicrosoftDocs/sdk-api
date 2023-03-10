---
UID: NF:mprapi.MprInfoBlockRemove
title: MprInfoBlockRemove function (mprapi.h)
description: The MprInfoBlockRemove function creates a new header that is identical to an existing header with a specified block removed.
helpviewer_keywords: ["MprInfoBlockRemove","MprInfoBlockRemove function [RAS]","_mpr_mprinfoblockremove","mprapi/MprInfoBlockRemove","rras.mprinfoblockremove"]
old-location: rras\mprinfoblockremove.htm
tech.root: RRAS
ms.assetid: 2d124541-c954-4031-95cd-68a96c8e0a77
ms.date: 12/05/2018
ms.keywords: MprInfoBlockRemove, MprInfoBlockRemove function [RAS], _mpr_mprinfoblockremove, mprapi/MprInfoBlockRemove, rras.mprinfoblockremove
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprInfoBlockRemove
 - mprapi/MprInfoBlockRemove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprInfoBlockRemove
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
<a href="/windows/desktop/RRAS/ip-information-types-for-router-information-blocks">IP</a> or 
<a href="/windows/desktop/RRAS/ipx-information-types-for-router-information-blocks">IPX</a>.

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
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a> could not be completed.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>

## -remarks

After removing an information block, obtain the new size of the information header by call 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockquerysize">MprInfoBlockQuerySize</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockadd">MprInfoBlockAdd</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockquerysize">MprInfoBlockQuerySize</a>