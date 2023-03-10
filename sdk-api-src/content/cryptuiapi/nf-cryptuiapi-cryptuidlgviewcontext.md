---
UID: NF:cryptuiapi.CryptUIDlgViewContext
title: CryptUIDlgViewContext function (cryptuiapi.h)
description: Displays a certificate, CTL, or CRL context.
helpviewer_keywords: ["CERT_STORE_CERTIFICATE_CONTEXT","CERT_STORE_CRL_CONTEXT","CERT_STORE_CTL_CONTEXT","CryptUIDlgViewContext","CryptUIDlgViewContext function [Security]","_crypto2_cryptuidlgviewcontext","cryptuiapi/CryptUIDlgViewContext","security.cryptuidlgviewcontext"]
old-location: security\cryptuidlgviewcontext.htm
tech.root: security
ms.assetid: d4b8f01b-7c3e-4286-bc37-d5ec4a1e1c2f
ms.date: 12/05/2018
ms.keywords: CERT_STORE_CERTIFICATE_CONTEXT, CERT_STORE_CRL_CONTEXT, CERT_STORE_CTL_CONTEXT, CryptUIDlgViewContext, CryptUIDlgViewContext function [Security], _crypto2_cryptuidlgviewcontext, cryptuiapi/CryptUIDlgViewContext, security.cryptuidlgviewcontext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptUIDlgViewContext
 - cryptuiapi/CryptUIDlgViewContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptui.dll
api_name:
 - CryptUIDlgViewContext
---

# CryptUIDlgViewContext function


## -description

The <b>CryptUIDlgViewContext</b> function displays a certificate, CTL, or CRL context.

## -parameters

### -param dwContextType [in]

<b>DWORD</b> indicating whether <i>pvContext</i> is a pointer to a certificate, a CRL, or a CTL context as indicated in the following table. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CERTIFICATE_CONTEXT"></a><a id="cert_store_certificate_context"></a><dl>
<dt><b>CERT_STORE_CERTIFICATE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
PCCERT_CONTEXT

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CRL_CONTEXT"></a><a id="cert_store_crl_context"></a><dl>
<dt><b>CERT_STORE_CRL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
PCCRL_CONTEXT

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTL_CONTEXT"></a><a id="cert_store_ctl_context"></a><dl>
<dt><b>CERT_STORE_CTL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
PCCTL_CONTEXT

</td>
</tr>
</table>

### -param pvContext [in]

A pointer to a certificate, CRL, or CTL context to be displayed.

### -param hwnd [in]

Handle of the window for the display. If <b>NULL</b>, the display defaults to the desktop window.

### -param pwszTitle [in]

Display title string. If <b>NULL</b>, the default context type is used as the title.

### -param dwFlags [in]

Currently not used and should be set to 0.

### -param pvReserved [in]

Reserved for future use.

## -returns

This function returns <b>TRUE</b> on success and <b>FALSE</b> on failure.

## -see-also

<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore">CryptUIDlgSelectCertificateFromStore</a>