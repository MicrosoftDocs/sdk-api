---
UID: NF:mssip.CryptSIPRemoveProvider
title: CryptSIPRemoveProvider function (mssip.h)
description: Removes registry details of a Subject Interface Package (SIP) DLL file added by a previous call to the CryptSIPAddProvider function.
helpviewer_keywords: ["CryptSIPRemoveProvider","CryptSIPRemoveProvider function [Security]","mssip/CryptSIPRemoveProvider","security.cryptsipremoveprovider"]
old-location: security\cryptsipremoveprovider.htm
tech.root: security
ms.assetid: 0a269956-b2c7-414a-b002-7cec0d52bfd6
ms.date: 12/05/2018
ms.keywords: CryptSIPRemoveProvider, CryptSIPRemoveProvider function [Security], mssip/CryptSIPRemoveProvider, security.cryptsipremoveprovider
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
 - CryptSIPRemoveProvider
 - mssip/CryptSIPRemoveProvider
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
 - CryptSIPRemoveProvider
---

# CryptSIPRemoveProvider function


## -description

The <b>CryptSIPRemoveProvider</b> function removes registry details of a Subject Interface Package (SIP) DLL file  added by a previous call to the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipaddprovider">CryptSIPAddProvider</a> function.

## -parameters

### -param pgProv [in]

A pointer to the GUID that identifies the SIP DLL  to remove.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to determine the reason for failure.

## -remarks

Typically you call this function to unregister an in-process COM server. The <b>CryptSIPRemoveProvider</b> function removes the appropriate Registry entries for the SIP provider functions.

## -see-also

<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipaddprovider">CryptSIPAddProvider</a>