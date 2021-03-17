---
UID: NF:aclapi.FreeInheritedFromArray
title: FreeInheritedFromArray function (aclapi.h)
description: Frees memory allocated by the GetInheritanceSource function.
helpviewer_keywords: ["FreeInheritedFromArray","FreeInheritedFromArray function [Security]","_win32_freeinheritedfromarray","aclapi/FreeInheritedFromArray","security.freeinheritedfromarray"]
old-location: security\freeinheritedfromarray.htm
tech.root: security
ms.assetid: c9c58b9a-1b65-40e2-b518-30e247f9718e
ms.date: 12/05/2018
ms.keywords: FreeInheritedFromArray, FreeInheritedFromArray function [Security], _win32_freeinheritedfromarray, aclapi/FreeInheritedFromArray, security.freeinheritedfromarray
req.header: aclapi.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeInheritedFromArray
 - aclapi/FreeInheritedFromArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - FreeInheritedFromArray
---

# FreeInheritedFromArray function


## -description

The <b>FreeInheritedFromArray</b> function frees memory allocated by the 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getinheritancesourcea">GetInheritanceSource</a> function.

## -parameters

### -param pInheritArray [in]

A pointer to the array of <a href="/windows/desktop/api/accctrl/ns-accctrl-inherited_froma">INHERITED_FROM</a> structures returned by <a href="/windows/desktop/api/aclapi/nf-aclapi-getinheritancesourcea">GetInheritanceSource</a>.

### -param AceCnt [in]

Number of entries in <i>pInheritArray</i>.

### -param pfnArray [in, optional]

Unused. Set to <b>NULL</b>.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/aclapi/nf-aclapi-getinheritancesourcea">GetInheritanceSource</a>