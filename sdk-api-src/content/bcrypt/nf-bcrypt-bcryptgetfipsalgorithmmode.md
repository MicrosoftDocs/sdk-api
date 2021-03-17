---
UID: NF:bcrypt.BCryptGetFipsAlgorithmMode
title: BCryptGetFipsAlgorithmMode function (bcrypt.h)
description: Determines whether Federal Information Processing Standard (FIPS) compliance is enabled.
helpviewer_keywords: ["BCryptGetFipsAlgorithmMode","BCryptGetFipsAlgorithmMode function [Security]","bcrypt/BCryptGetFipsAlgorithmMode","security.bcryptgetfipsalgorithmmode"]
old-location: security\bcryptgetfipsalgorithmmode.htm
tech.root: security
ms.assetid: eb7b758d-3466-49fe-8729-a8a059fadcde
ms.date: 12/05/2018
ms.keywords: BCryptGetFipsAlgorithmMode, BCryptGetFipsAlgorithmMode function [Security], bcrypt/BCryptGetFipsAlgorithmMode, security.bcryptgetfipsalgorithmmode
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
 - BCryptGetFipsAlgorithmMode
 - bcrypt/BCryptGetFipsAlgorithmMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptGetFipsAlgorithmMode
---

# BCryptGetFipsAlgorithmMode function


## -description

The <b>BCryptGetFipsAlgorithmMode</b> function determines whether Federal Information Processing Standard (FIPS) compliance is enabled.

## -parameters

### -param pfEnabled [out]

The address of a <b>BOOLEAN</b> variable that receives zero if FIPS compliance is not enabled, or a nonzero value if FIPS compliance is enabled.

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
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfEnabled</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

<b>BCryptGetFipsAlgorithmMode</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>.