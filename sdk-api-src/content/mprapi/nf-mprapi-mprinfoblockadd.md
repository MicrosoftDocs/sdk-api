---
UID: NF:mprapi.MprInfoBlockAdd
title: MprInfoBlockAdd function (mprapi.h)
description: The MprInfoBlockAdd function creates a new header that is identical to an existing header with the addition of a new block.
helpviewer_keywords: ["MprInfoBlockAdd","MprInfoBlockAdd function [RAS]","_mpr_mprinfoblockadd","mprapi/MprInfoBlockAdd","rras.mprinfoblockadd"]
old-location: rras\mprinfoblockadd.htm
tech.root: RRAS
ms.assetid: 94d8fc3b-1ed6-4555-85c0-40e32d197a72
ms.date: 12/05/2018
ms.keywords: MprInfoBlockAdd, MprInfoBlockAdd function [RAS], _mpr_mprinfoblockadd, mprapi/MprInfoBlockAdd, rras.mprinfoblockadd
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
 - MprInfoBlockAdd
 - mprapi/MprInfoBlockAdd
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
 - MprInfoBlockAdd
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
<a href="/windows/desktop/RRAS/ip-information-types-for-router-information-blocks">IPv4</a>, <a href="/windows/desktop/RRAS/ipv6-information-types-for-router-information-blocks">IPv6</a>, or <a href="/windows/desktop/RRAS/ipx-information-types-for-router-information-blocks">IPX</a>.

<b>Windows Server 2008:  </b>If <i>dwInfoTYpe</i> contains <a href="/windows/desktop/RRAS/ip-information-types-for-router-information-blocks">IP_ROUTE_INFO</a>, <i>lpItemData</i> must point to a <a href="/openspecs/windows_protocols/ms-rrasm/784d8544-140a-4769-b659-7d3168de9242">INTERFACE_ROUTE_INFO</a> structure.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the error message that corresponds to the returned error code.

</td>
</tr>
</table>

## -remarks

After adding an information block, obtain the new size of the information header by call 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockquerysize">MprInfoBlockQuerySize</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/RRAS/understanding-mprinfo-functions-and-information-headers">MprInfo Functions and Information Headers</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockquerysize">MprInfoBlockQuerySize</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoblockremove">MprInfoBlockRemove</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprinfoduplicate">MprInfoDuplicate</a>