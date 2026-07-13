---
UID: NS:cryptuiapi.tagCRYPTUI_VIEWCERTIFICATE_STRUCTW
title: CRYPTUI_VIEWCERTIFICATE_STRUCTW (cryptuiapi.h)
description: Contains information about a certificate to view. This structure is used in the CryptUIDlgViewCertificate function. (Unicode)
helpviewer_keywords: ["*PCRYPTUI_VIEWCERTIFICATE_STRUCTW","CRYPTUI_ACCEPT_DECLINE_STYLE","CRYPTUI_CACHE_ONLY_URL_RETRIEVAL","CRYPTUI_DISABLE_ADDTOSTORE","CRYPTUI_DISABLE_EDITPROPERTIES","CRYPTUI_DISABLE_EXPORT","CRYPTUI_DISABLE_HTMLLINK","CRYPTUI_DISABLE_ISSUERSTATEMENT","CRYPTUI_DONT_OPEN_STORES","CRYPTUI_ENABLE_ADDTOSTORE","CRYPTUI_ENABLE_EDITPROPERTIES","CRYPTUI_ENABLE_REVOCATION_CHECKING","CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN","CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT","CRYPTUI_ENABLE_REVOCATION_CHECK_END_CERT","CRYPTUI_HIDE_DETAILPAGE","CRYPTUI_HIDE_HIERARCHYPAGE","CRYPTUI_IGNORE_UNTRUSTED_ROOT","CRYPTUI_ONLY_OPEN_ROOT_STORE","CRYPTUI_VIEWCERTIFICATE_STRUCT","CRYPTUI_VIEWCERTIFICATE_STRUCT structure [Security]","CRYPTUI_VIEWCERTIFICATE_STRUCTA","CRYPTUI_VIEWCERTIFICATE_STRUCTW","CRYPTUI_WARN_REMOTE_TRUST","CRYPTUI_WARN_UNTRUSTED_ROOT","PCCRYPTUI_VIEWCERTIFICATE_STRUCT","PCCRYPTUI_VIEWCERTIFICATE_STRUCT structure pointer [Security]","PCRYPTUI_VIEWCERTIFICATE_STRUCT","PCRYPTUI_VIEWCERTIFICATE_STRUCT structure pointer [Security]","cryptuiapi/CRYPTUI_VIEWCERTIFICATE_STRUCT","cryptuiapi/CRYPTUI_VIEWCERTIFICATE_STRUCTA","cryptuiapi/CRYPTUI_VIEWCERTIFICATE_STRUCTW","cryptuiapi/PCCRYPTUI_VIEWCERTIFICATE_STRUCT","cryptuiapi/PCRYPTUI_VIEWCERTIFICATE_STRUCT","security.cryptui_viewcertificate_struct","security.cryptui_viewcertificate_structw"]
old-location: security\cryptui_viewcertificate_struct.htm
tech.root: security
ms.assetid: 7bbd58df-3a1b-4d82-9a90-7c94260a7165
ms.date: 12/05/2018
ms.keywords: '*PCRYPTUI_VIEWCERTIFICATE_STRUCTW, CRYPTUI_ACCEPT_DECLINE_STYLE, CRYPTUI_CACHE_ONLY_URL_RETRIEVAL, CRYPTUI_DISABLE_ADDTOSTORE, CRYPTUI_DISABLE_EDITPROPERTIES, CRYPTUI_DISABLE_EXPORT, CRYPTUI_DISABLE_HTMLLINK, CRYPTUI_DISABLE_ISSUERSTATEMENT, CRYPTUI_DONT_OPEN_STORES, CRYPTUI_ENABLE_ADDTOSTORE, CRYPTUI_ENABLE_EDITPROPERTIES, CRYPTUI_ENABLE_REVOCATION_CHECKING, CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN, CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT, CRYPTUI_ENABLE_REVOCATION_CHECK_END_CERT, CRYPTUI_HIDE_DETAILPAGE, CRYPTUI_HIDE_HIERARCHYPAGE, CRYPTUI_IGNORE_UNTRUSTED_ROOT, CRYPTUI_ONLY_OPEN_ROOT_STORE, CRYPTUI_VIEWCERTIFICATE_STRUCT, CRYPTUI_VIEWCERTIFICATE_STRUCT structure [Security], CRYPTUI_VIEWCERTIFICATE_STRUCTA, CRYPTUI_VIEWCERTIFICATE_STRUCTW, CRYPTUI_WARN_REMOTE_TRUST, CRYPTUI_WARN_UNTRUSTED_ROOT, PCCRYPTUI_VIEWCERTIFICATE_STRUCT, PCCRYPTUI_VIEWCERTIFICATE_STRUCT structure pointer [Security], PCRYPTUI_VIEWCERTIFICATE_STRUCT, PCRYPTUI_VIEWCERTIFICATE_STRUCT structure pointer [Security], cryptuiapi/CRYPTUI_VIEWCERTIFICATE_STRUCT, cryptuiapi/CRYPTUI_VIEWCERTIFICATE_STRUCTA, cryptuiapi/CRYPTUI_VIEWCERTIFICATE_STRUCTW, cryptuiapi/PCCRYPTUI_VIEWCERTIFICATE_STRUCT, cryptuiapi/PCRYPTUI_VIEWCERTIFICATE_STRUCT, security.cryptui_viewcertificate_struct, security.cryptui_viewcertificate_structw'
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CRYPTUI_VIEWCERTIFICATE_STRUCTW (Unicode) and CRYPTUI_VIEWCERTIFICATE_STRUCTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPTUI_VIEWCERTIFICATE_STRUCTW, *PCRYPTUI_VIEWCERTIFICATE_STRUCTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCRYPTUI_VIEWCERTIFICATE_STRUCTW
 - cryptuiapi/tagCRYPTUI_VIEWCERTIFICATE_STRUCTW
 - PCRYPTUI_VIEWCERTIFICATE_STRUCTW
 - cryptuiapi/PCRYPTUI_VIEWCERTIFICATE_STRUCTW
 - CRYPTUI_VIEWCERTIFICATE_STRUCTW
 - cryptuiapi/CRYPTUI_VIEWCERTIFICATE_STRUCTW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptuiapi.h
api_name:
 - CRYPTUI_VIEWCERTIFICATE_STRUCT
 - CRYPTUI_VIEWCERTIFICATE_STRUCTA
 - CRYPTUI_VIEWCERTIFICATE_STRUCTW
---

# CRYPTUI_VIEWCERTIFICATE_STRUCTW structure


## -description

The <b>CRYPTUI_VIEWCERTIFICATE_STRUCT</b> structure contains information about a certificate to view.  This structure is used in the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a> function.

## -struct-fields

### -field dwSize

The size, in bytes, of the <b>CRYPTUI_VIEWCERTIFICATE_STRUCT</b> structure.

### -field hwndParent

A handle to the window that is the parent of the dialog box produced by <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a>.

### -field dwFlags

 This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_HIDE_HIERARCHYPAGE"></a><a id="cryptui_hide_hierarchypage"></a><dl>
<dt><b>CRYPTUI_HIDE_HIERARCHYPAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>Certification Path</b> page is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_HIDE_DETAILPAGE"></a><a id="cryptui_hide_detailpage"></a><dl>
<dt><b>CRYPTUI_HIDE_DETAILPAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>Details</b> page is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_DISABLE_EDITPROPERTIES"></a><a id="cryptui_disable_editproperties"></a><dl>
<dt><b>CRYPTUI_DISABLE_EDITPROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
 The user is not allowed to change the properties.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ENABLE_EDITPROPERTIES"></a><a id="cryptui_enable_editproperties"></a><dl>
<dt><b>CRYPTUI_ENABLE_EDITPROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
The user is allowed to change the properties.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_DISABLE_ADDTOSTORE"></a><a id="cryptui_disable_addtostore"></a><dl>
<dt><b>CRYPTUI_DISABLE_ADDTOSTORE</b></dt>
</dl>
</td>
<td width="60%">
The <b>Install</b> button is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ENABLE_ADDTOSTORE"></a><a id="cryptui_enable_addtostore"></a><dl>
<dt><b>CRYPTUI_ENABLE_ADDTOSTORE</b></dt>
</dl>
</td>
<td width="60%">
The <b>Install</b> button is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ACCEPT_DECLINE_STYLE"></a><a id="cryptui_accept_decline_style"></a><dl>
<dt><b>CRYPTUI_ACCEPT_DECLINE_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The pages or buttons that allow the user to accept or decline any decision are disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_IGNORE_UNTRUSTED_ROOT"></a><a id="cryptui_ignore_untrusted_root"></a><dl>
<dt><b>CRYPTUI_IGNORE_UNTRUSTED_ROOT</b></dt>
</dl>
</td>
<td width="60%">
An untrusted root error is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_DONT_OPEN_STORES"></a><a id="cryptui_dont_open_stores"></a><dl>
<dt><b>CRYPTUI_DONT_OPEN_STORES</b></dt>
</dl>
</td>
<td width="60%">
Known trusted stores will not be used to build the chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ONLY_OPEN_ROOT_STORE"></a><a id="cryptui_only_open_root_store"></a><dl>
<dt><b>CRYPTUI_ONLY_OPEN_ROOT_STORE</b></dt>
</dl>
</td>
<td width="60%">
A known trusted root store will not be used to build the chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WARN_UNTRUSTED_ROOT"></a><a id="cryptui_warn_untrusted_root"></a><dl>
<dt><b>CRYPTUI_WARN_UNTRUSTED_ROOT</b></dt>
</dl>
</td>
<td width="60%">
Use only when viewing  certificates on remote
computers.  If this flag is used, the first element of <b>rghStores</b> must be the handle of the root store on the remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ENABLE_REVOCATION_CHECKING"></a><a id="cryptui_enable_revocation_checking"></a><dl>
<dt><b>CRYPTUI_ENABLE_REVOCATION_CHECKING</b></dt>
</dl>
</td>
<td width="60%">
Enable revocation checking with default behavior.  The default behavior is to enable revocation checking of the entire certificate chain except the root certificate.  Valid only if neither the  <b>pCryptProviderData</b> nor the <b>hWVTStateData</b> union member is  passed in.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WARN_REMOTE_TRUST"></a><a id="cryptui_warn_remote_trust"></a><dl>
<dt><b>CRYPTUI_WARN_REMOTE_TRUST</b></dt>
</dl>
</td>
<td width="60%">
When building a certificate chain for a remote computer, warn that the chain may not be trusted on the remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_DISABLE_EXPORT"></a><a id="cryptui_disable_export"></a><dl>
<dt><b>CRYPTUI_DISABLE_EXPORT</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>Copy to file</b> button will be
disabled on the <b>Detail</b> page.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ENABLE_REVOCATION_CHECK_END_CERT"></a><a id="cryptui_enable_revocation_check_end_cert"></a><dl>
<dt><b>CRYPTUI_ENABLE_REVOCATION_CHECK_END_CERT</b></dt>
</dl>
</td>
<td width="60%">
Enable revocation checking only on the leaf certificate in the certificate chain. Valid only if neither  the <b>pCryptProviderData</b> nor the <b>hWVTStateData</b> union member is  passed in.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN"></a><a id="cryptui_enable_revocation_check_chain"></a><dl>
<dt><b>CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
Enable revocation checking on each certificate in the certificate chain.  Valid only if neither the  <b>pCryptProviderData</b> nor the <b>hWVTStateData</b> union member is  passed in.

<b>Note</b>  Because root certificates rarely contain information that allows revocation checking, it is expected that use of this option will usually result in failure of the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a> function.  The recommended option is to use CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT"></a><a id="cryptui_enable_revocation_check_chain_exclude_root"></a><dl>
<dt><b>CRYPTUI_ENABLE_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT</b></dt>
</dl>
</td>
<td width="60%">
Enable revocation checking on each certificate in the certificate chain except for the root certificate. This is the recommended option to use for certificate revocation checking.  Valid only if neither the  <b>pCryptProviderData</b> nor the <b>hWVTStateData</b> union member is  passed in.

<b>Note</b>  This flag is equivalent to CRYPTUI_ENABLE_REVOCATION_CHECKING.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_DISABLE_HTMLLINK"></a><a id="cryptui_disable_htmllink"></a><dl>
<dt><b>CRYPTUI_DISABLE_HTMLLINK</b></dt>
</dl>
</td>
<td width="60%">
Disable the HTML Help button (<b>?</b>)  in the <b>Certificate</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_DISABLE_ISSUERSTATEMENT"></a><a id="cryptui_disable_issuerstatement"></a><dl>
<dt><b>CRYPTUI_DISABLE_ISSUERSTATEMENT</b></dt>
</dl>
</td>
<td width="60%">
Disable the <b>Issuer Statement</b> button on the <b>General</b> tab of the <b>Certificate</b> dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_CACHE_ONLY_URL_RETRIEVAL"></a><a id="cryptui_cache_only_url_retrieval"></a><dl>
<dt><b>CRYPTUI_CACHE_ONLY_URL_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Disable online revocation checking. Set this flag to ensure that the <a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a> function uses the local cache to retrieve the certificate and  does not attempt to retrieve the certificate from the network.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
</table>

### -field szTitle

A pointer to a null-terminated string that contains the title for the window.

### -field pCertContext

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the certificate context to display.

### -field rgszPurposes

An array of pointers to null-terminated strings that contain the purposes for which this certificate will be validated.

### -field cPurposes

The number of purposes in the <b>rgszPurposes</b> array.

### -field pCryptProviderData

If the <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> function has already been called for the certificate and the <a href="/windows/desktop/api/wintrust/nf-wintrust-wthelperprovdatafromstatedata">WTHelperProvDataFromStateData</a> function was also called, pass in a pointer to the state structure that was acquired from the call to <b>WTHelperProvDataFromStateData</b>. If <b>pCryptProviderData</b> is set,  <b>fpCryptProviderDataTrustedUsage</b>, <b>idxSigner</b>, <b>idxCert</b>, and <b>fCounterSignature</b> must also be set.

### -field hWVTStateData

If <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> has already been called for the certificate and <a href="/windows/desktop/api/wintrust/nf-wintrust-wthelperprovdatafromstatedata">WTHelperProvDataFromStateData</a> was not called, pass in the <b>hWVTStateData</b> member of the <a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_data">WINTRUST_DATA</a> structure. If <b>hWVTStateData</b> is set,  <b>fpCryptProviderDataTrustedUsage</b>, <b>idxSigner</b>, <b>idxCert</b>, and <b>fCounterSignature</b> must also be set.

### -field fpCryptProviderDataTrustedUsage

If <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> was called, this is the result of whether the certificate was trusted.

### -field idxSigner

The index of the signer to view.

### -field idxCert

The index of the certificate that is being viewed within the signer chain.  The certificate context of this cert must match <b>pCertContext</b>.

### -field fCounterSigner

<b>TRUE</b> if a countersignature is being viewed.  If  this is <b>TRUE</b>, <b>idxCounterSigner</b> must be valid.

### -field idxCounterSigner

The index of the countersigner to view.

### -field cStores

The number of other stores in the  <b>rghStores</b> array of certificate stores to search when building and validating the certificate chain.

### -field rghStores

An array of <b>HCERTSTORE</b> handles to other certificate stores to search when building and validating the certificate chain.

### -field cPropSheetPages

The number of property pages to add to the dialog box.

### -field rgPropSheetPages

An array of property pages to add to the dialog box.                        Each page in this array will not receive the <b>lParam</b> in the <a href="/windows/desktop/api/prsht/ns-prsht-propsheetpagea_v2">PROPSHEETPAGE</a> structure as the <b>lParam</b> in the <a href="/windows/desktop/dlgbox/wm-initdialog">WM_INITDIALOG</a> message. It will instead receive a pointer to a <a href="/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cryptui_initdialog_struct">CRYPTUI_INITDIALOG_STRUCT</a>  structure. It contains the <b>lParam</b> in  <b>PROPSHEETPAGE</b> and the pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> for which the page is being displayed.

### -field nStartPage

The index of the initial page that will be displayed.  If the highest bit (0x8000) is set, the index is assumed to index <b>rgPropSheetPages</b> (after the highest bit has been stripped off, for example, 0x8000 will indicate the first page in <b>rgPropSheetPages</b>).  If the highest bit is zero,  <b>nStartPage</b> will be the starting index of the default certificate dialog box property pages.

## -see-also

<a href="/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea">CryptUIDlgViewCertificate</a>

## -remarks

> [!NOTE]
> The cryptuiapi.h header defines CRYPTUI_VIEWCERTIFICATE_STRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
