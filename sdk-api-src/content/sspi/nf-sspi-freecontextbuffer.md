---
UID: NF:sspi.FreeContextBuffer
title: FreeContextBuffer function (sspi.h)
description: Enables callers of security package functions to free memory buffers allocated by the security package.
helpviewer_keywords: ["FreeContextBuffer","FreeContextBuffer function [Security]","_ssp_freecontextbuffer","security.freecontextbuffer","sspi/FreeContextBuffer"]
old-location: security\freecontextbuffer.htm
tech.root: security
ms.assetid: 3c3d27bb-4f9a-4979-b679-1e10fa1ff221
ms.date: 12/05/2018
ms.keywords: FreeContextBuffer, FreeContextBuffer function [Security], _ssp_freecontextbuffer, security.freecontextbuffer, sspi/FreeContextBuffer
req.header: sspi.h
req.include-header: Security.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FreeContextBuffer
 - sspi/FreeContextBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - FreeContextBuffer
---

# FreeContextBuffer function


## -description

The <b>FreeContextBuffer</b> function enables callers of <a href="/windows/desktop/SecGloss/s-gly">security package</a> functions to free memory buffers allocated by the security package.

## -parameters

### -param pvContextBuffer [in]

A pointer to memory to be freed.

## -returns

If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns a nonzero error code.

## -remarks

Memory buffers are typically allocated by the  <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> and <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> functions.

The <b>FreeContextBuffer</b> function can free any memory allocated by a security package.

## -see-also

<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>