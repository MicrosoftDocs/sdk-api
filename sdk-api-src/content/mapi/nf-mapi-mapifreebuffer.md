---
UID: NF:mapi.MAPIFreeBuffer
title: MAPIFreeBuffer function (mapi.h)
description: The MAPIFreeBuffer function (mapi.h) frees memory allocated by the messaging system.
helpviewer_keywords: ["MAPIFreeBuffer","MAPIFreeBuffer callback","MAPIFreeBuffer callback function","mapi.mapifreebuffer","wabmem/MAPIFreeBuffer"]
old-location: mapi\mapifreebuffer.htm
tech.root: mapi
ms.assetid: b67a2a42-edba-4372-b3b7-5bf3e9d3e5ed
ms.date: 08/03/2022
ms.keywords: MAPIFreeBuffer, MAPIFreeBuffer callback, MAPIFreeBuffer callback function, mapi.mapifreebuffer, wabmem/MAPIFreeBuffer
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
req.lib: MAPI32.Lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAPIFreeBuffer
 - mapi/MAPIFreeBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - wabmem.h
api_name:
 - MAPIFreeBuffer
---

# MAPIFreeBuffer function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIFreeBuffer</b> function frees memory allocated by the messaging system.

## -parameters

### -param pv [in]

Pointer to memory allocated by the messaging system. This pointer is returned by the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapireadmail">MAPIReadMail</a>, <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiaddress">MAPIAddress</a>, and <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapiresolvename">MAPIResolveName</a> functions.

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

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogoff">MAPILogoff</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>
