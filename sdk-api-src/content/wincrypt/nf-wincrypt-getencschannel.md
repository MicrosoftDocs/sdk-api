---
UID: NF:wincrypt.GetEncSChannel
title: GetEncSChannel function (wincrypt.h)
description: This function is unavailable.
helpviewer_keywords: ["GetEncSChannel","GetEncSChannel function [Security]","security.getencschannel","wincrypt/GetEncSChannel"]
old-location: security\getencschannel.htm
tech.root: security
ms.assetid: 4879895e-8bf4-4464-a344-04e4b361c5c7
ms.date: 12/05/2018
ms.keywords: GetEncSChannel, GetEncSChannel function [Security], security.getencschannel, wincrypt/GetEncSChannel
req.header: wincrypt.h
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
req.lib: 
req.dll: Instrsa5.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetEncSChannel
 - wincrypt/GetEncSChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Instrsa5.dll
api_name:
 - GetEncSChannel
---

# GetEncSChannel function


## -description

<p class="CCE_Message">[The GetEncSChannel function is no longer available for use as of Windows Server 2003 and Windows XP.]
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Instrsa5.dll.</div><div> </div>

## -parameters

### -param pData [out]

A pointer to a pointer to bytes that receive the encrypted Schannel contents. When you have finished using the Schannel contents, free <i>pData</i> by calling the <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a> function.

### -param dwDecSize [out]

Number of bytes allocated for <i>pData</i>.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>