---
UID: NF:wintrust.WTHelperProvDataFromStateData
title: WTHelperProvDataFromStateData function (wintrust.h)
description: Retrieves trust provider information from a specified handle.
helpviewer_keywords: ["WTHelperProvDataFromStateData","WTHelperProvDataFromStateData function [Security]","security.wthelperprovdatafromstatedata","wintrust/WTHelperProvDataFromStateData"]
old-location: security\wthelperprovdatafromstatedata.htm
tech.root: security
ms.assetid: ca2ca612-2da6-4fe1-8b1e-bc6307eb92af
ms.date: 12/05/2018
ms.keywords: WTHelperProvDataFromStateData, WTHelperProvDataFromStateData function [Security], security.wthelperprovdatafromstatedata, wintrust/WTHelperProvDataFromStateData
req.header: wintrust.h
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WTHelperProvDataFromStateData
 - wintrust/WTHelperProvDataFromStateData
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
 - WTHelperProvDataFromStateData
---

# WTHelperProvDataFromStateData function


## -description

<p class="CCE_Message">[The <b>WTHelperProvDataFromStateData</b> function is available for use in  the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WTHelperProvDataFromStateData</b> function retrieves trust provider information from a specified handle. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hStateData [in]

A handle previously set by the <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrustex">WinVerifyTrustEx</a> function as the <b>hWVTStateData</b>	 member of the <a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_data">WINTRUST_DATA</a> structure.

## -returns

If the function succeeds, the function returns a pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a> structure. The returned pointer can be used by the <a href="/windows/desktop/api/wintrust/nf-wintrust-wthelpergetprovsignerfromchain">WTHelperGetProvSignerFromChain</a>   function.

If the function fails, it returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wintrust/nf-wintrust-wthelpergetprovsignerfromchain">WTHelperGetProvSignerFromChain</a>