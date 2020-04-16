---
UID: NF:cryptuiapi.CryptUIWizFreeDigitalSignContext
title: CryptUIWizFreeDigitalSignContext function (cryptuiapi.h)
description: Frees the CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT structure allocated by the CryptUIWizDigitalSign function.helpviewer_keywords: ["CryptUIWizFreeDigitalSignContext","CryptUIWizFreeDigitalSignContext function [Security]","cryptuiapi/CryptUIWizFreeDigitalSignContext","security.cryptuiwizfreedigitalsigncontext"]
old-location: security\cryptuiwizfreedigitalsigncontext.htm
tech.root: SecCrypto
ms.assetid: 039615ee-0485-4698-944f-23359253767a
ms.date: 12/05/2018
ms.keywords: CryptUIWizFreeDigitalSignContext, CryptUIWizFreeDigitalSignContext function [Security], cryptuiapi/CryptUIWizFreeDigitalSignContext, security.cryptuiwizfreedigitalsigncontext
f1_keywords:
- cryptuiapi/CryptUIWizFreeDigitalSignContext
dev_langs:
- c++
req.header: cryptuiapi.h
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
req.lib: Cryptui.lib
req.dll: Cryptui.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Cryptui.dll
api_name:
- CryptUIWizFreeDigitalSignContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptUIWizFreeDigitalSignContext function


## -description


The <b>CryptUIWizFreeDigitalSignContext</b> function frees the <a href="https://docs.microsoft.com/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a> structure allocated by the <a href="https://docs.microsoft.com/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a> function.


## -parameters




### -param pSignContext [in]

A pointer to the   <a href="https://docs.microsoft.com/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a> structure to be freed.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign">CryptUIWizDigitalSign</a>
 

 

