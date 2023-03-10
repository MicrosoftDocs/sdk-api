---
UID: NS:wintrust._WINTRUST_DATA
title: WINTRUST_DATA (wintrust.h)
description: Used when calling WinVerifyTrust to pass necessary information into the trust providers.
helpviewer_keywords: ["*PWINTRUST_DATA","PWINTRUST_DATA","PWINTRUST_DATA structure pointer [Security]","WINTRUST_DATA","WINTRUST_DATA structure [Security]","WTD_CACHE_ONLY_URL_RETRIEVAL","WTD_CHOICE_BLOB","WTD_CHOICE_CATALOG","WTD_CHOICE_CERT","WTD_CHOICE_FILE","WTD_CHOICE_SIGNER","WTD_DISABLE_MD2_MD4","WTD_HASH_ONLY_FLAG","WTD_LIFETIME_SIGNING_FLAG","WTD_MOTW","WTD_NO_IE4_CHAIN_FLAG","WTD_NO_POLICY_USAGE_FLAG","WTD_REVOCATION_CHECK_CHAIN","WTD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT","WTD_REVOCATION_CHECK_END_CERT","WTD_REVOCATION_CHECK_NONE","WTD_REVOKE_NONE","WTD_REVOKE_WHOLECHAIN","WTD_SAFER_FLAG","WTD_STATEACTION_AUTO_CACHE","WTD_STATEACTION_AUTO_CACHE_FLUSH","WTD_STATEACTION_CLOSE","WTD_STATEACTION_IGNORE","WTD_STATEACTION_VERIFY","WTD_UICONTEXT_EXECUTE","WTD_UICONTEXT_INSTALL","WTD_UI_ALL","WTD_UI_NOBAD","WTD_UI_NOGOOD","WTD_UI_NONE","WTD_USE_DEFAULT_OSVER_CHECK","WTD_USE_IE4_TRUST_FLAG","_win32_wintrust_data","security.wintrust_data","wintrust/PWINTRUST_DATA","wintrust/WINTRUST_DATA"]
old-location: security\wintrust_data.htm
tech.root: security
ms.assetid: 8fb68f44-6f69-4eac-90de-02689e3e86cf
ms.date: 12/05/2018
ms.keywords: '*PWINTRUST_DATA, PWINTRUST_DATA, PWINTRUST_DATA structure pointer [Security], WINTRUST_DATA, WINTRUST_DATA structure [Security], WTD_CACHE_ONLY_URL_RETRIEVAL, WTD_CHOICE_BLOB, WTD_CHOICE_CATALOG, WTD_CHOICE_CERT, WTD_CHOICE_FILE, WTD_CHOICE_SIGNER, WTD_DISABLE_MD2_MD4, WTD_HASH_ONLY_FLAG, WTD_LIFETIME_SIGNING_FLAG, WTD_MOTW, WTD_NO_IE4_CHAIN_FLAG, WTD_NO_POLICY_USAGE_FLAG, WTD_REVOCATION_CHECK_CHAIN, WTD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT, WTD_REVOCATION_CHECK_END_CERT, WTD_REVOCATION_CHECK_NONE, WTD_REVOKE_NONE, WTD_REVOKE_WHOLECHAIN, WTD_SAFER_FLAG, WTD_STATEACTION_AUTO_CACHE, WTD_STATEACTION_AUTO_CACHE_FLUSH, WTD_STATEACTION_CLOSE, WTD_STATEACTION_IGNORE, WTD_STATEACTION_VERIFY, WTD_UICONTEXT_EXECUTE, WTD_UICONTEXT_INSTALL, WTD_UI_ALL, WTD_UI_NOBAD, WTD_UI_NOGOOD, WTD_UI_NONE, WTD_USE_DEFAULT_OSVER_CHECK, WTD_USE_IE4_TRUST_FLAG, _win32_wintrust_data, security.wintrust_data, wintrust/PWINTRUST_DATA, wintrust/WINTRUST_DATA'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINTRUST_DATA, *PWINTRUST_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINTRUST_DATA
 - wintrust/_WINTRUST_DATA
 - PWINTRUST_DATA
 - wintrust/PWINTRUST_DATA
 - WINTRUST_DATA
 - wintrust/WINTRUST_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_DATA
---

# WINTRUST_DATA structure


## -description

<p class="CCE_Message">[The  <b>WINTRUST_DATA</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_DATA</b> structure is used when calling 
<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> to pass necessary information into the <a href="/windows/desktop/SecGloss/t-gly">trust providers</a>.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field pPolicyCallbackData

A pointer to a data buffer used to pass policy-specific data to a policy provider. This member can be <b>NULL</b>.

### -field pSIPClientData

A pointer to a data buffer used to pass <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP)-specific data to a SIP provider. This member can be <b>NULL</b>.

### -field dwUIChoice

Specifies the kind of user interface (UI) to be used. This member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTD_UI_ALL"></a><a id="wtd_ui_all"></a><dl>
<dt><b>WTD_UI_ALL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Display all UI.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_UI_NONE"></a><a id="wtd_ui_none"></a><dl>
<dt><b>WTD_UI_NONE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Display no UI.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_UI_NOBAD"></a><a id="wtd_ui_nobad"></a><dl>
<dt><b>WTD_UI_NOBAD</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Do not display any negative UI.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_UI_NOGOOD"></a><a id="wtd_ui_nogood"></a><dl>
<dt><b>WTD_UI_NOGOOD</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Do not display any positive UI.

</td>
</tr>
</table>

### -field fdwRevocationChecks

Certificate revocation check options. This member can be set to add revocation checking to that done by the selected policy provider. This member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTD_REVOKE_NONE"></a><a id="wtd_revoke_none"></a><dl>
<dt><b>WTD_REVOKE_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No additional revocation checking will be done when the <b>WTD_REVOKE_NONE</b> flag is used in conjunction with the <b>HTTPSPROV_ACTION</b> value set in the <i>pgActionID</i> parameter of the <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> function. To ensure the <b>WinVerifyTrust</b> function does not attempt any network retrieval when verifying code signatures, <b>WTD_CACHE_ONLY_URL_RETRIEVAL</b> must be set in the <i>dwProvFlags</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_REVOKE_WHOLECHAIN"></a><a id="wtd_revoke_wholechain"></a><dl>
<dt><b>WTD_REVOKE_WHOLECHAIN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Revocation checking will be done on the whole chain.

</td>
</tr>
</table>

### -field dwUnionChoice

Specifies the union member to be used and, thus, the type of object for which trust will be verified. This member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTD_CHOICE_FILE"></a><a id="wtd_choice_file"></a><dl>
<dt><b>WTD_CHOICE_FILE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use the file pointed to by <b>pFile</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_CHOICE_CATALOG"></a><a id="wtd_choice_catalog"></a><dl>
<dt><b>WTD_CHOICE_CATALOG</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Use the catalog pointed to by <b>pCatalog</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_CHOICE_BLOB"></a><a id="wtd_choice_blob"></a><dl>
<dt><b>WTD_CHOICE_BLOB</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Use the <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> pointed to by <b>pBlob</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_CHOICE_SIGNER"></a><a id="wtd_choice_signer"></a><dl>
<dt><b>WTD_CHOICE_SIGNER</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Use the [WINTRUST_SGNR_INFO](/windows/desktop/api/wintrust/ns-wintrust-wintrust_sgnr_info) structure pointed to by <b>pSgnr</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_CHOICE_CERT"></a><a id="wtd_choice_cert"></a><dl>
<dt><b>WTD_CHOICE_CERT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Use the certificate pointed to by <b>pCert</b>.

</td>
</tr>
</table>

### -field pFile

A pointer to a 
<a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_file_info">WINTRUST_FILE_INFO</a> structure.

### -field pCatalog

A pointer to a 
<a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_catalog_info">WINTRUST_CATALOG_INFO</a> structure.

### -field pBlob

A pointer to a 
<a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_blob_info">WINTRUST_BLOB_INFO</a> structure.

### -field pSgnr

A pointer to a 
[WINTRUST_SGNR_INFO](/windows/desktop/api/wintrust/ns-wintrust-wintrust_sgnr_info) structure.

### -field pCert

A pointer to a 
<a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_cert_info">WINTRUST_CERT_INFO</a> structure.

### -field dwStateAction

Specifies the action to be taken. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTD_STATEACTION_IGNORE"></a><a id="wtd_stateaction_ignore"></a><dl>
<dt><b>WTD_STATEACTION_IGNORE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Ignore the <b>hWVTStateData</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_STATEACTION_VERIFY"></a><a id="wtd_stateaction_verify"></a><dl>
<dt><b>WTD_STATEACTION_VERIFY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Verify the trust of the object (typically a file) that is specified by the <b>dwUnionChoice</b> member. The <b>hWVTStateData</b> member will receive a handle to the state data. This handle must be freed by specifying the <b>WTD_STATEACTION_CLOSE</b> action in a subsequent call.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_STATEACTION_CLOSE"></a><a id="wtd_stateaction_close"></a><dl>
<dt><b>WTD_STATEACTION_CLOSE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Free the <b>hWVTStateData</b> member previously allocated with the <b>WTD_STATEACTION_VERIFY</b> action. This action must be specified for every use of the <b>WTD_STATEACTION_VERIFY</b> action.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_STATEACTION_AUTO_CACHE"></a><a id="wtd_stateaction_auto_cache"></a><dl>
<dt><b>WTD_STATEACTION_AUTO_CACHE</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Write the catalog data to a <b>WINTRUST_DATA</b> structure and then cache that structure. This action only applies when the <b>dwUnionChoice</b> member contains <b>WTD_CHOICE_CATALOG</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_STATEACTION_AUTO_CACHE_FLUSH"></a><a id="wtd_stateaction_auto_cache_flush"></a><dl>
<dt><b>WTD_STATEACTION_AUTO_CACHE_FLUSH</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Flush any cached catalog data. This action only applies when the <b>dwUnionChoice</b> member contains <b>WTD_CHOICE_CATALOG</b>.

</td>
</tr>
</table>

### -field hWVTStateData

A handle to the state data. The contents of this member depends on the value of the <b>dwStateAction</b> member.

### -field pwszURLReference

Reserved for future use. Set to <b>NULL</b>.

### -field dwProvFlags

<b>DWORD</b> value that specifies trust provider settings. This can be a bitwise combination of zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTD_USE_IE4_TRUST_FLAG"></a><a id="wtd_use_ie4_trust_flag"></a><dl>
<dt><b>WTD_USE_IE4_TRUST_FLAG</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The trust is verified in the same manner as implemented by Internet Explorer 4.0.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_NO_IE4_CHAIN_FLAG"></a><a id="wtd_no_ie4_chain_flag"></a><dl>
<dt><b>WTD_NO_IE4_CHAIN_FLAG</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The Internet Explorer 4.0 chain functionality is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_NO_POLICY_USAGE_FLAG"></a><a id="wtd_no_policy_usage_flag"></a><dl>
<dt><b>WTD_NO_POLICY_USAGE_FLAG</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The default verification of the policy provider, such as code signing for <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a>, is not performed, and  the certificate is assumed valid for all usages.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_REVOCATION_CHECK_NONE"></a><a id="wtd_revocation_check_none"></a><dl>
<dt><b>WTD_REVOCATION_CHECK_NONE</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Revocation checking is not performed.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_REVOCATION_CHECK_END_CERT"></a><a id="wtd_revocation_check_end_cert"></a><dl>
<dt><b>WTD_REVOCATION_CHECK_END_CERT</b></dt>
<dt>32 (0x20)</dt>
</dl>
</td>
<td width="60%">
Revocation checking is performed on the end certificate only.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_REVOCATION_CHECK_CHAIN"></a><a id="wtd_revocation_check_chain"></a><dl>
<dt><b>WTD_REVOCATION_CHECK_CHAIN</b></dt>
<dt>64 (0x40)</dt>
</dl>
</td>
<td width="60%">
Revocation checking is performed on the entire certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT"></a><a id="wtd_revocation_check_chain_exclude_root"></a><dl>
<dt><b>WTD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT</b></dt>
<dt>128 (0x80)</dt>
</dl>
</td>
<td width="60%">
Revocation checking is performed on the entire certificate chain,  excluding the root certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_SAFER_FLAG"></a><a id="wtd_safer_flag"></a><dl>
<dt><b>WTD_SAFER_FLAG</b></dt>
<dt>256 (0x100)</dt>
</dl>
</td>
<td width="60%">
Not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_HASH_ONLY_FLAG"></a><a id="wtd_hash_only_flag"></a><dl>
<dt><b>WTD_HASH_ONLY_FLAG</b></dt>
<dt>512 (0x200)</dt>
</dl>
</td>
<td width="60%">
Only the hash is verified.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_USE_DEFAULT_OSVER_CHECK"></a><a id="wtd_use_default_osver_check"></a><dl>
<dt><b>WTD_USE_DEFAULT_OSVER_CHECK</b></dt>
<dt>1024 (0x400)</dt>
</dl>
</td>
<td width="60%">
The default operating system version checking is performed. This flag is only used for verifying catalog-signed files.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_LIFETIME_SIGNING_FLAG"></a><a id="wtd_lifetime_signing_flag"></a><dl>
<dt><b>WTD_LIFETIME_SIGNING_FLAG</b></dt>
<dt>2048 (0x800)</dt>
</dl>
</td>
<td width="60%">
If this flag is not set,  all time stamped signatures are considered valid forever. Setting this flag limits the valid lifetime of the signature to the lifetime of the signing certificate. This allows time stamped signatures to expire.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_CACHE_ONLY_URL_RETRIEVAL"></a><a id="wtd_cache_only_url_retrieval"></a><dl>
<dt><b>WTD_CACHE_ONLY_URL_RETRIEVAL</b></dt>
<dt>4096 (0x1000)</dt>
</dl>
</td>
<td width="60%">
Use only the local cache for revocation checks. Prevents revocation checks over the network. 

<b>Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_DISABLE_MD2_MD4"></a><a id="wtd_disable_md2_md4"></a><dl>
<dt><b>WTD_DISABLE_MD2_MD4</b></dt>
<dt>8192 (0x2000)</dt>
</dl>
</td>
<td width="60%">
Disable the use of MD2 and MD4 hashing algorithms. If a file is signed by using MD2 or MD4 and if this flag is set, an NTE_BAD_ALGID error is returned.

<div class="alert"><b>Note</b>  This flag is supported on Windows 7 with SP1 and later operating systems.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="WTD_MOTW"></a><a id="wtd_motw"></a><dl>
<dt><b>WTD_MOTW</b></dt>
<dt>16384 (0x4000)</dt>
</dl>
</td>
<td width="60%">
If this flag is specified it is assumed that the file being verified has been downloaded from the web and has the Mark of the Web attribute. Policies that are meant to apply to Mark of the Web files will be enforced.


<div class="alert"><b>Note</b>  This flag is supported on Windows 8.1 and later operating systems or on systems that have installed KB2862966.</div>
<div> </div>
</td>
</tr>
</table>

### -field dwUIContext

A <b>DWORD</b> value that specifies the user interface context for the <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> function. This causes the text in the Authenticode dialog box to match the action taken on the file. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WTD_UICONTEXT_EXECUTE"></a><a id="wtd_uicontext_execute"></a><dl>
<dt><b>WTD_UICONTEXT_EXECUTE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Use when calling <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> for a file that is  to be run.  This is the default value.

</td>
</tr>
<tr>
<td width="40%"><a id="WTD_UICONTEXT_INSTALL"></a><a id="wtd_uicontext_install"></a><dl>
<dt><b>WTD_UICONTEXT_INSTALL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use when calling <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> for a file that is  to be installed.

</td>
</tr>
</table>

### -field pSignatureSettings

Pointer to a [WINTRUST_SIGNATURE_SETTINGS](/windows/desktop/api/wintrust/ns-wintrust-wintrust_signature_settings) structure.

<b>Windows 8 and Windows Server 2012:  </b>Support for this member begins.