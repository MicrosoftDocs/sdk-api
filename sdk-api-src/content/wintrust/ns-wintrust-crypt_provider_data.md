---
UID: NS:wintrust._CRYPT_PROVIDER_DATA
title: CRYPT_PROVIDER_DATA (wintrust.h)
description: Used to pass data between WinVerifyTrust and trust providers.
helpviewer_keywords: ["*PCRYPT_PROVIDER_DATA","CPD_REVOCATION_CHECK_CHAIN","CPD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT","CPD_REVOCATION_CHECK_END_CERT","CPD_REVOCATION_CHECK_NONE","CPD_USE_NT5_CHAIN_FLAG","CRYPT_PROVIDER_DATA","CRYPT_PROVIDER_DATA structure [Security]","PCRYPT_PROVIDER_DATA","PCRYPT_PROVIDER_DATA structure pointer [Security]","security.crypt_provider_data","wintrust/CRYPT_PROVIDER_DATA","wintrust/PCRYPT_PROVIDER_DATA"]
old-location: security\crypt_provider_data.htm
tech.root: security
ms.assetid: 93ea2ad5-65da-4daa-bfd4-e3d1307829b2
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_DATA, CPD_REVOCATION_CHECK_CHAIN, CPD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT, CPD_REVOCATION_CHECK_END_CERT, CPD_REVOCATION_CHECK_NONE, CPD_USE_NT5_CHAIN_FLAG, CRYPT_PROVIDER_DATA, CRYPT_PROVIDER_DATA structure [Security], PCRYPT_PROVIDER_DATA, PCRYPT_PROVIDER_DATA structure pointer [Security], security.crypt_provider_data, wintrust/CRYPT_PROVIDER_DATA, wintrust/PCRYPT_PROVIDER_DATA'
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
req.typenames: CRYPT_PROVIDER_DATA, *PCRYPT_PROVIDER_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_DATA
 - wintrust/_CRYPT_PROVIDER_DATA
 - PCRYPT_PROVIDER_DATA
 - wintrust/PCRYPT_PROVIDER_DATA
 - CRYPT_PROVIDER_DATA
 - wintrust/CRYPT_PROVIDER_DATA
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
 - CRYPT_PROVIDER_DATA
---

# CRYPT_PROVIDER_DATA structure


## -description

<p class="CCE_Message">[The  <b>CRYPT_PROVIDER_DATA</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVIDER_DATA</b> structure is used to pass data between <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> and trust providers.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field pWintrustData

A pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_data">WINTRUST_DATA</a> structure that contains the information to verify.

### -field fOpenedFile

A Boolean value that indicates whether the trust provider opened the file handle, if applicable.

### -field hWndParent

A handle to the parent window. If not specified, a handle to the desktop  window is used.

### -field pgActionID

A pointer to a <b>GUID</b> structure that identifies an action and the trust provider that supports that action.

### -field hProv

A handle to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). If this parameter is <b>NULL</b>, then the operating system will provide a default CSP.

### -field dwError

An error level if a low-level system error was encountered.

### -field dwRegSecuritySettings

The registry security settings.

### -field dwRegPolicySettings

The registry policy settings.

### -field psPfns

A pointer to a <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_functions">CRYPT_PROVIDER_FUNCTIONS</a> structure.

### -field cdwTrustStepErrors

The number of elements in the <b>padwTrustStepErrors</b> array.

### -field padwTrustStepErrors

An array of <b>DWORD</b> values that specify trust step errors.

### -field chStores

The number of elements in the <b>pahStores</b> array.

### -field pahStores

An array of certificate store handles.

### -field dwEncoding

A value that specifies the encoding type.

### -field hMsg

A  handle to the cryptographic message.

### -field csSigners

The number of elements in the <b>pasSigners</b> array.

### -field pasSigners

A pointer to an array of <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_sgnr">CRYPT_PROVIDER_SGNR</a> structures.

### -field csProvPrivData

The number of elements in the <b>pasProvPrivData</b> array.

### -field pasProvPrivData

A pointer to an array of <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_privdata">CRYPT_PROVIDER_PRIVDATA</a> structures.

### -field dwSubjectChoice

A value that specifies the subject choice.

### -field pPDSip

A pointer to a <b>_PROVDATA_SIP</b> structure.

### -field pszUsageOID

A pointer to a null-terminated string that contains the usage <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

### -field fRecallWithState

A Boolean value that indicates whether state was maintained for catalog files.

### -field sftSystemTime

The system time.

### -field pszCTLSignerUsageOID

A pointer to a null-terminated string that represents the <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) signer usage OID.

### -field dwProvFlags

A bitwise combination of one or more of the following flags.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CPD_USE_NT5_CHAIN_FLAG"></a><a id="cpd_use_nt5_chain_flag"></a><dl>
<dt><b>CPD_USE_NT5_CHAIN_FLAG</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Use Windows 2000 chaining.

</td>
</tr>
<tr>
<td width="40%"><a id="CPD_REVOCATION_CHECK_NONE"></a><a id="cpd_revocation_check_none"></a><dl>
<dt><b>CPD_REVOCATION_CHECK_NONE</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
No revocation checking is performed.

</td>
</tr>
<tr>
<td width="40%"><a id="CPD_REVOCATION_CHECK_END_CERT"></a><a id="cpd_revocation_check_end_cert"></a><dl>
<dt><b>CPD_REVOCATION_CHECK_END_CERT</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Revocation checking for the end certificate is performed.

</td>
</tr>
<tr>
<td width="40%"><a id="CPD_REVOCATION_CHECK_CHAIN"></a><a id="cpd_revocation_check_chain"></a><dl>
<dt><b>CPD_REVOCATION_CHECK_CHAIN</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Revocation checking for the  certificate chain is performed.

</td>
</tr>
<tr>
<td width="40%"><a id="CPD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT"></a><a id="cpd_revocation_check_chain_exclude_root"></a><dl>
<dt><b>CPD_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Revocation checking for the  certificate chain, excluding the root certificate,  is performed.

</td>
</tr>
</table>

### -field dwFinalError

A value for the final error.

### -field pRequestUsage

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_usage_match">CERT_USAGE_MATCH</a> structure.

### -field dwTrustPubSettings

A value for the trust publisher settings.

### -field dwUIStateFlags

A <b>DWORD</b> value that specifies state data that is passed between a trust provider and the user interface.

<b>Windows XP with SP1 and Windows XP:  </b>This member is ignored.

### -field pSigState

### -field pSigSettings