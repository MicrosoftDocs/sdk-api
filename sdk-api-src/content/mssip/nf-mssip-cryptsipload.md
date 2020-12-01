---
UID: NF:mssip.CryptSIPLoad
title: CryptSIPLoad function (mssip.h)
description: Loads the dynamic-link library (DLL) that implements a subject interface package (SIP) and assigns appropriate library export functions to a SIP_DISPATCH_INFO structure.
helpviewer_keywords: ["CryptSIPLoad","CryptSIPLoad function [Security]","mssip/CryptSIPLoad","security.cryptsipload"]
old-location: security\cryptsipload.htm
tech.root: security
ms.assetid: 3378ecee-bd5d-45e5-9a1f-a3734d086782
ms.date: 12/05/2018
ms.keywords: CryptSIPLoad, CryptSIPLoad function [Security], mssip/CryptSIPLoad, security.cryptsipload
req.header: mssip.h
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptSIPLoad
 - mssip/CryptSIPLoad
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptSIPLoad
---

# CryptSIPLoad function


## -description

The [SIP_DISPATCH_INFO](/windows/desktop/api/mssip/ns-mssip-sip_dispatch_info) structure. The exported functions must have been previously registered by calling the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipaddprovider">CryptSIPAddProvider</a> function.

## -parameters

### -param pgSubject [in]

A pointer to a GUID returned by calling the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipretrievesubjectguid">CryptSIPRetrieveSubjectGuid</a> function.

### -param dwFlags [in]

This parameter is reserved and must be set to zero.

### -param pSipDispatch [in, out]

A pointer to a [SIP_DISPATCH_INFO](/windows/desktop/api/mssip/ns-mssip-sip_dispatch_info) structure that contains pointers to SIP provider functions that are specific to the subject type. The caller must initialize this structure to binary zeros, and set the <b>cbSize</b> member to <code>sizeof(SIP_DISPATCH_INFO)</code> before calling the <b>CryptSIPLoad</b> function.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.