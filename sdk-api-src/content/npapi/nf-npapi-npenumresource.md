---
UID: NF:npapi.NPEnumResource
title: NPEnumResource function (npapi.h)
description: Performs an enumeration based on a handle returned by NPOpenEnum.
helpviewer_keywords: ["NPEnumResource","NPEnumResource function [Security]","_mnp_npenumresource","npapi/NPEnumResource","security.npenumresource"]
old-location: security\npenumresource.htm
tech.root: security
ms.assetid: 286a6865-478a-41e5-a48f-42f9fc117f14
ms.date: 12/05/2018
ms.keywords: NPEnumResource, NPEnumResource function [Security], _mnp_npenumresource, npapi/NPEnumResource, security.npenumresource
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: davclnt.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPEnumResource
 - npapi/NPEnumResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPEnumResource
---

# NPEnumResource function


## -description

Performs an enumeration based on a handle returned by 
<a href="/windows/desktop/api/npapi/nf-npapi-npopenenum">NPOpenEnum</a>.

## -parameters

### -param hEnum [in]

Handle obtained from an 
<a href="/windows/desktop/api/npapi/nf-npapi-npopenenum">NPOpenEnum</a> call.

### -param lpcCount [in, out]

Pointer to the number of entries requested. It may be 0xFFFFFFFF to request as many entries as possible. If the call succeeds, this location will receive the number of entries actually read.

### -param lpBuffer [out]

Pointer to the buffer to receive the enumeration result, which is returned as an array of 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> entries. The buffer is valid until the next call using <i>hEnum</i>.

### -param lpBufferSize [in, out]

Pointer to the size, in bytes, of the buffer passed to the function call on entry. If the buffer is too small for even one entry, this should contain, on exit, the number of bytes needed to read one entry. This value is  set only if the return code is WN_MORE_DATA.

## -returns

If the function succeeds, it should return WN_SUCCESS. The caller may continue to call <b>NPEnumResource</b> to continue the enumeration. Otherwise, it should return one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
No more entries. The enumeration was completed successfully. When this occurs, the contents of the return buffer, <i>lpBuffer</i>, are undefined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to hold even a single entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_BAD_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hEnum</i> is not a valid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present. This condition is checked  before <i>hEnum</i> is tested for validity.

</td>
</tr>
</table>

## -remarks

When this function is called, the provider should fill the buffer with the requested number of entries (or the maximum that can fit). The returned 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structures should be located contiguously at the head of the buffer, like an array of such structures. The pointers in these structures must point to locations within the buffer. Therefore, data referenced by these pointers should be located at the end of the buffer, after the array of structures. It is the provider's responsibility to package this information correctly.