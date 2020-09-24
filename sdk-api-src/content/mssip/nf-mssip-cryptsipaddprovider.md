---
UID: NF:mssip.CryptSIPAddProvider
title: CryptSIPAddProvider function (mssip.h)
description: The CryptSIPAddProvider function registers functions that are exported by a given DLL file that implements a Subject Interface Package (SIP).
helpviewer_keywords: ["CryptSIPAddProvider","CryptSIPAddProvider function [Security]","mssip/CryptSIPAddProvider","security.cryptsipaddprovider"]
old-location: security\cryptsipaddprovider.htm
tech.root: security
ms.assetid: 99633c2f-e5ed-49e4-9c98-7501f66e5571
ms.date: 12/05/2018
ms.keywords: CryptSIPAddProvider, CryptSIPAddProvider function [Security], mssip/CryptSIPAddProvider, security.cryptsipaddprovider
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
 - CryptSIPAddProvider
 - mssip/CryptSIPAddProvider
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
 - CryptSIPAddProvider
---

# CryptSIPAddProvider function


## -description

The <b>CryptSIPAddProvider</b> function registers functions that are exported by a given DLL file that implements  a Subject Interface Package (SIP).

## -parameters

### -param psNewProv [in]

A pointer to a [SIP_ADD_NEWPROVIDER](/windows/desktop/api/mssip/ns-mssip-sip_add_newprovider) structure that specifies the DLL file and function names to register.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to determine the reason for failure.

## -remarks

Typically, you call this function as part of an in-process COM server registration. The <b>CryptSIPAddProvider</b> function persists the appropriate Registry entries for the SIP provider functions.

When you have finished using the added SIP provider, remove it by calling the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipremoveprovider">CryptSIPRemoveProvider</a> function.

## -see-also

<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipremoveprovider">CryptSIPRemoveProvider</a>