---
UID: NF:cryptuiapi.CryptUIDlgSelectCertificateFromStore
title: CryptUIDlgSelectCertificateFromStore function (cryptuiapi.h)
description: Displays a dialog box that allows the selection of a certificate from a specified store.
helpviewer_keywords: ["CRYPTUI_SELECT_EXPIRATION_COLUMN","CRYPTUI_SELECT_FRIENDLYNAME_COLUMN","CRYPTUI_SELECT_INTENDEDUSE_COLUMN","CRYPTUI_SELECT_ISSUEDBY_COLUMN","CRYPTUI_SELECT_ISSUEDTO_COLUMN","CRYPTUI_SELECT_LOCATION_COLUMN","CryptUIDlgSelectCertificateFromStore","CryptUIDlgSelectCertificateFromStore function [Security]","_crypto2_cryptuidlgselectcertificatefromstore","cryptuiapi/CryptUIDlgSelectCertificateFromStore","security.cryptuidlgselectcertificatefromstore"]
old-location: security\cryptuidlgselectcertificatefromstore.htm
tech.root: security
ms.assetid: 5774af1c-f2d4-4b1e-a20b-dfb57bf9aa37
ms.date: 12/05/2018
ms.keywords: CRYPTUI_SELECT_EXPIRATION_COLUMN, CRYPTUI_SELECT_FRIENDLYNAME_COLUMN, CRYPTUI_SELECT_INTENDEDUSE_COLUMN, CRYPTUI_SELECT_ISSUEDBY_COLUMN, CRYPTUI_SELECT_ISSUEDTO_COLUMN, CRYPTUI_SELECT_LOCATION_COLUMN, CryptUIDlgSelectCertificateFromStore, CryptUIDlgSelectCertificateFromStore function [Security], _crypto2_cryptuidlgselectcertificatefromstore, cryptuiapi/CryptUIDlgSelectCertificateFromStore, security.cryptuidlgselectcertificatefromstore
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
 - CryptUIDlgSelectCertificateFromStore
 - cryptuiapi/CryptUIDlgSelectCertificateFromStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptui.dll
 - Ext-MS-Win-security-cryptui-l1-1-0.dll
 - ext-ms-win-security-cryptui-l1-1-1.dll
 - CertCredProviderOneCore.dll
api_name:
 - CryptUIDlgSelectCertificateFromStore
---

# CryptUIDlgSelectCertificateFromStore function


## -description

The <b>CryptUIDlgSelectCertificateFromStore</b> function displays a dialog box that allows the selection of a certificate from a specified store.

## -parameters

### -param hCertStore [in]

Handle of the certificate store to be searched.

### -param hwnd [in]

Handle of the window for the display. If <b>NULL</b>, defaults to the desktop window.

### -param pwszTitle [in, optional]

String used as the title of the dialog box. If <b>NULL</b>, the default title, "Select Certificate," is used.

### -param pwszDisplayString [in, optional]

Text statement in the selection dialog box. If <b>NULL</b>, the default phrase, "Select a certificate you want to use," is used.

### -param dwDontUseColumn [in]

Flags that can be combined to exclude columns of the display. 



					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></a><a id="cryptui_select_issuedto_column"></a><dl>
<dt><b>CRYPTUI_SELECT_ISSUEDTO_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display the ISSUEDTO information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></a><a id="cryptui_select_issuedby_column"></a><dl>
<dt><b>CRYPTUI_SELECT_ISSUEDBY_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display the ISSUEDBY information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></a><a id="cryptui_select_intendeduse_column"></a><dl>
<dt><b>CRYPTUI_SELECT_INTENDEDUSE_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display IntendedUse information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></a><a id="cryptui_select_friendlyname_column"></a><dl>
<dt><b>CRYPTUI_SELECT_FRIENDLYNAME_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display the display name information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_LOCATION_COLUMN"></a><a id="cryptui_select_location_column"></a><dl>
<dt><b>CRYPTUI_SELECT_LOCATION_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display location information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></a><a id="cryptui_select_expiration_column"></a><dl>
<dt><b>CRYPTUI_SELECT_EXPIRATION_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display expiration information.

</td>
</tr>
</table>

### -param dwFlags [in]

Currently not used and should be set to 0.

### -param pvReserved [in]

Reserved for future use.

## -returns

Returns a pointer to the selected certificate context. If no certificate was selected, <b>NULL</b> is returned. When you have finished using the certificate, free the certificate context by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

## -see-also

<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext">CryptUIDlgViewContext</a>