---
UID: NF:cryptuiapi.CryptUIWizDigitalSign
title: CryptUIWizDigitalSign function (cryptuiapi.h)
description: Digitally signs a document or BLOB.
helpviewer_keywords: ["CRYPTUI_WIZ_NO_UI","CryptUIWizDigitalSign","CryptUIWizDigitalSign function [Security]","cryptuiapi/CryptUIWizDigitalSign","security.cryptuiwizdigitalsign"]
old-location: security\cryptuiwizdigitalsign.htm
tech.root: security
ms.assetid: 1d01523e-d47b-49be-82c8-5e98f97be800
ms.date: 12/05/2018
ms.keywords: CRYPTUI_WIZ_NO_UI, CryptUIWizDigitalSign, CryptUIWizDigitalSign function [Security], cryptuiapi/CryptUIWizDigitalSign, security.cryptuiwizdigitalsign
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
 - CryptUIWizDigitalSign
 - cryptuiapi/CryptUIWizDigitalSign
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
 - CryptUIWizDigitalSign
---

# CryptUIWizDigitalSign function


## -description

<p class="CCE_Message">[The  <b>CryptUIWizDigitalSign</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptUIWizDigitalSign</b> function digitally signs a document or <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>. The document or BLOB can be signed with or without user interaction.

## -parameters

### -param dwFlags [in]

Contains flags that modify the behavior of the function. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_NO_UI"></a><a id="cryptui_wiz_no_ui"></a><dl>
<dt><b>CRYPTUI_WIZ_NO_UI</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
This function will sign the document based on the information in the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_info">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a> structure pointed to by the <i>pDigitalSignInfo</i> parameter without displaying any user interface. If this flag is not specified, this function will display a wizard to guide the user through the signing process.

</td>
</tr>
</table>

### -param hwndParent [in, optional]

The handle of the window to use as the parent of the dialog box that  this function creates. This parameter is ignored if the <b>CRYPTUI_WIZ_NO_UI</b> flag is set in <i>dwFlags</i>.

### -param pwszWizardTitle [in, optional]

A pointer to a null-terminated Unicode string that contains the title to use in the dialog box that this function creates. This parameter is ignored if the <b>CRYPT_WIZ_NO_UI</b> flag is set in <i>dwFlags</i>. If this parameter is <b>NULL</b>, a default title is used.

### -param pDigitalSignInfo [in]

A pointer to a <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_info">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a> structure that contains information about the signing process.

### -param ppSignContext [out, optional]

A pointer to a <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a> structure pointer that receives the signed BLOB. When you have finished using this structure, you must free the memory by passing this pointer to the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext">CryptUIWizFreeDigitalSignContext</a> function. This parameter can be <b>NULL</b> if the signed BLOB is not needed.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context">CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</a>



<a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_info">CRYPTUI_WIZ_DIGITAL_SIGN_INFO</a>



<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext">CryptUIWizFreeDigitalSignContext</a>
