---
UID: NF:bcrypt.BCryptCloseAlgorithmProvider
title: BCryptCloseAlgorithmProvider function (bcrypt.h)
description: Closes an algorithm provider.
helpviewer_keywords: ["BCryptCloseAlgorithmProvider","BCryptCloseAlgorithmProvider function [Security]","bcrypt/BCryptCloseAlgorithmProvider","security.bcryptclosealgorithmprovider_func"]
old-location: security\bcryptclosealgorithmprovider_func.htm
tech.root: security
ms.assetid: def90d52-87e0-40e6-9c50-fd77177991d0
ms.date: 12/05/2018
ms.keywords: BCryptCloseAlgorithmProvider, BCryptCloseAlgorithmProvider function [Security], bcrypt/BCryptCloseAlgorithmProvider, security.bcryptclosealgorithmprovider_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptCloseAlgorithmProvider
 - bcrypt/BCryptCloseAlgorithmProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptCloseAlgorithmProvider
---

# BCryptCloseAlgorithmProvider function


## -description

The <b>BCryptCloseAlgorithmProvider</b> function closes an algorithm provider.

## -parameters

### -param hAlgorithm [in, out]

A handle that represents the algorithm provider to close. This handle is obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The algorithm handle in the <i>hAlgorithm</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

<b>BCryptCloseAlgorithmProvider</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="https://www.microsoft.com/?ref=go">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a>