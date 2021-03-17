---
UID: NF:wintrust.WintrustLoadFunctionPointers
title: WintrustLoadFunctionPointers function (wintrust.h)
description: Loads function entry points for a specified action GUID. This function has no associated import library.
helpviewer_keywords: ["HTTPSPROV_ACTION","WINTRUST_ACTION_GENERIC_VERIFY","WINTRUST_ACTION_GENERIC_VERIFY_V2","WintrustLoadFunctionPointers","WintrustLoadFunctionPointers function [Security]","security.wintrustloadfunctionpointers","wintrust/WintrustLoadFunctionPointers"]
old-location: security\wintrustloadfunctionpointers.htm
tech.root: security
ms.assetid: c36db226-34b4-4a31-b8c6-b9d124acc669
ms.date: 12/05/2018
ms.keywords: HTTPSPROV_ACTION, WINTRUST_ACTION_GENERIC_VERIFY, WINTRUST_ACTION_GENERIC_VERIFY_V2, WintrustLoadFunctionPointers, WintrustLoadFunctionPointers function [Security], security.wintrustloadfunctionpointers, wintrust/WintrustLoadFunctionPointers
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
 - WintrustLoadFunctionPointers
 - wintrust/WintrustLoadFunctionPointers
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
 - WintrustLoadFunctionPointers
---

# WintrustLoadFunctionPointers function


## -description

<p class="CCE_Message">[The <b>WintrustLoadFunctionPointers</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions. For Microsoft <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> technology signature verification, use the .NET Framework.]

The <b>WintrustLoadFunctionPointers</b> function loads function entry points for a specified action GUID. This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param pgActionID [in]

A pointer to a <b>GUID</b> structure that identifies the action whose function pointers are being loaded and the <a href="/windows/desktop/SecGloss/t-gly">trust provider</a> that supports that action.

The WinTrust service is designed to work with trust providers implemented by third parties. Each trust provider provides its own unique set of action identifiers. For information about the action identifiers supported by a trust provider, see the documentation for that trust provider.

For example, Microsoft provides a Software Publisher Trust Provider that can establish the trustworthiness of software being downloaded from the Internet or some other public network. The Software Publisher Trust Provider supports the following action identifiers. These constants are defined in Softpub.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINTRUST_ACTION_GENERIC_VERIFY"></a><a id="wintrust_action_generic_verify"></a><dl>
<dt><b>WINTRUST_ACTION_GENERIC_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Verify a certificate chain only.

</td>
</tr>
<tr>
<td width="40%"><a id="WINTRUST_ACTION_GENERIC_VERIFY_V2"></a><a id="wintrust_action_generic_verify_v2"></a><dl>
<dt><b>WINTRUST_ACTION_GENERIC_VERIFY_V2</b></dt>
</dl>
</td>
<td width="60%">
Verify a file or object using the Authenticode policy provider.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTPSPROV_ACTION"></a><a id="httpsprov_action"></a><dl>
<dt><b>HTTPSPROV_ACTION</b></dt>
</dl>
</td>
<td width="60%">
Verify an SSL/PCT connection through Internet Explorer.

</td>
</tr>
</table>

### -param pPfns [out]

A pointer to the <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_functions">CRYPT_PROVIDER_FUNCTIONS</a> structure that receives the addresses of the function pointers.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails.