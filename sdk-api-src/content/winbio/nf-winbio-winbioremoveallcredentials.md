---
UID: NF:winbio.WinBioRemoveAllCredentials
title: WinBioRemoveAllCredentials function (winbio.h)
description: Removes all credentials from the store. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WinBioRemoveAllCredentials","WinBioRemoveAllCredentials function [Windows Biometric Framework API]","secbiomet.winbioremoveallcredentials","winbio/WinBioRemoveAllCredentials"]
old-location: secbiomet\winbioremoveallcredentials.htm
tech.root: SecBioMet
ms.assetid: 3c3f3bed-531a-4962-8eb3-bebe16bed3a8
ms.date: 12/05/2018
ms.keywords: WinBioRemoveAllCredentials, WinBioRemoveAllCredentials function [Windows Biometric Framework API], secbiomet.winbioremoveallcredentials, winbio/WinBioRemoveAllCredentials
req.header: winbio.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioRemoveAllCredentials
 - winbio/WinBioRemoveAllCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-biometrics-winbio-core-l1-1-6.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-5.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-4.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-3.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-2.dll
 - Winbio.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioRemoveAllCredentials
---

# WinBioRemoveAllCredentials function


## -description

Removes all credentials from the store. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.



## -returns

If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioremovealldomaincredentials">WinBioRemoveAllDomainCredentials</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioremovecredential">WinBioRemoveCredential</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbiosetcredential">WinBioSetCredential</a>
