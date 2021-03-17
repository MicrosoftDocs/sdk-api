---
UID: NF:mprapi.MprInfoBlockSet
title: MprInfoBlockSet function (mprapi.h)
description: The MprInfoBlockSet creates a new header that is identical to an existing header with a specified block modified.
helpviewer_keywords: ["MprInfoBlockSet","MprInfoBlockSet function [RAS]","_mpr_mprinfoblockset","mprapi/MprInfoBlockSet","rras.mprinfoblockset"]
old-location: rras\mprinfoblockset.htm
tech.root: RRAS
ms.assetid: 55912927-d886-46d1-a5c1-e10f19c117ab
ms.date: 12/05/2018
ms.keywords: MprInfoBlockSet, MprInfoBlockSet function [RAS], _mpr_mprinfoblockset, mprapi/MprInfoBlockSet, rras.mprinfoblockset
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
 - MprInfoBlockSet
 - mprapi/MprInfoBlockSet
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
 - MprInfoBlockSet
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
<a href="/windows/desktop/RRAS/ip-information-types-for-router-information-blocks">IP</a> or 
<a href="/windows/desktop/RRAS/ipx-information-types-for-router-information-blocks">IPX</a>.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockadd">MprInfoBlockAdd</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a>