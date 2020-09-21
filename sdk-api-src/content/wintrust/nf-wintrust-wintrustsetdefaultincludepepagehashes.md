---
UID: NF:wintrust.WintrustSetDefaultIncludePEPageHashes
title: WintrustSetDefaultIncludePEPageHashes function (wintrust.h)
description: Sets the default setting that determines whether page hashes are included when creating subject interface package (SIP) indirect data for PE files.
helpviewer_keywords: ["WintrustSetDefaultIncludePEPageHashes","WintrustSetDefaultIncludePEPageHashes function [Security]","security.wintrustsetdefaultincludepepagehashes","wintrust/WintrustSetDefaultIncludePEPageHashes"]
old-location: security\wintrustsetdefaultincludepepagehashes.htm
tech.root: security
ms.assetid: af48e570-e71d-488f-831c-35834242db3c
ms.date: 12/05/2018
ms.keywords: WintrustSetDefaultIncludePEPageHashes, WintrustSetDefaultIncludePEPageHashes function [Security], security.wintrustsetdefaultincludepepagehashes, wintrust/WintrustSetDefaultIncludePEPageHashes
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WintrustSetDefaultIncludePEPageHashes
 - wintrust/WintrustSetDefaultIncludePEPageHashes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - WintrustSetDefaultIncludePEPageHashes
---

# WintrustSetDefaultIncludePEPageHashes function


## -description

The <b>WintrustSetDefaultIncludePEPageHashes</b> function sets the default setting that determines whether page hashes are included when creating subject interface package (SIP) indirect data for PE files.

This setting is only used if neither the <b>SPC_EXC_PE_PAGE_HASHES_FLAG</b> or the <b>SPC_INC_PE_PAGE_HASHES_FLAG</b> flag is specified in the <i>dwFlags</i> parameter of the <a href="/windows/desktop/SecCrypto/signersignex">SignerSignEx</a> function.

 This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param fIncludePEPageHashes [in]

Determines whether page hashes are included when creating SIP indirect data for PE files. If this parameter is nonzero, page hashes are included. If this parameter is zero, page hashes are not included. The value is zero by default.

## -remarks

This setting applies to each instance of Wintrust.dll.

## -see-also

<a href="/windows/desktop/SecCrypto/signersignex">SignerSignEx</a>