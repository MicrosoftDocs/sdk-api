---
UID: NF:ncryptprotect.NCryptStreamClose
title: NCryptStreamClose function (ncryptprotect.h)
description: Closes a data protection stream object opened by using the NCryptStreamOpenToProtect or NCryptStreamOpenToUnprotect functions.
helpviewer_keywords: ["NCryptStreamClose","NCryptStreamClose function [Security]","ncryptprotect/NCryptStreamClose","security.ncryptstreamclose"]
old-location: security\ncryptstreamclose.htm
tech.root: security
ms.assetid: 770640F2-04C7-4512-8004-41F4ECDC110E
ms.date: 12/05/2018
ms.keywords: NCryptStreamClose, NCryptStreamClose function [Security], ncryptprotect/NCryptStreamClose, security.ncryptstreamclose
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptStreamClose
 - ncryptprotect/NCryptStreamClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptStreamClose
---

# NCryptStreamClose function


## -description

The <b>NCryptStreamClose</b> function closes a data protection stream object opened by using the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> or <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a> functions.

## -parameters

### -param hStream [in]

Data stream handle returned by <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> or <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>.

## -returns

Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hStream</i> parameter is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a>