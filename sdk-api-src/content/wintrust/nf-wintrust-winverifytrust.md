---
UID: NF:wintrust.WinVerifyTrust
title: WinVerifyTrust function (wintrust.h)
description: Performs a trust verification action on a specified object.
helpviewer_keywords: ["A valid window handle","DRIVER_ACTION_VERIFY","HTTPSPROV_ACTION","INVALID_HANDLE_VALUE","OFFICESIGN_ACTION_VERIFY","WINTRUST_ACTION_GENERIC_CHAIN_VERIFY","WINTRUST_ACTION_GENERIC_VERIFY_V2","WINTRUST_ACTION_TRUSTPROVIDER_TEST","WinVerifyTrust","WinVerifyTrust function [Security]","Zero","_win32_winverifytrust","security.winverifytrust","wintrust/WinVerifyTrust"]
old-location: security\winverifytrust.htm
tech.root: security
ms.assetid: b7efac6a-ac9f-477a-aada-63fe32208e6f
ms.date: 12/05/2018
ms.keywords: A valid window handle, DRIVER_ACTION_VERIFY, HTTPSPROV_ACTION, INVALID_HANDLE_VALUE, OFFICESIGN_ACTION_VERIFY, WINTRUST_ACTION_GENERIC_CHAIN_VERIFY, WINTRUST_ACTION_GENERIC_VERIFY_V2, WINTRUST_ACTION_TRUSTPROVIDER_TEST, WinVerifyTrust, WinVerifyTrust function [Security], Zero, _win32_winverifytrust, security.winverifytrust, wintrust/WinVerifyTrust
req.header: wintrust.h
req.include-header: Softpub.h
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
 - WinVerifyTrust
 - wintrust/WinVerifyTrust
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
 - WinVerifyTrust
---

# WinVerifyTrust function


## -description

The <b>WinVerifyTrust</b> function performs a trust verification action on a specified object. The function passes the inquiry to a <a href="/windows/desktop/SecGloss/t-gly">trust provider</a> that supports the action identifier, if one exists.

For certificate verification, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy">CertVerifyCertificateChainPolicy</a> functions.

## -parameters

### -param hwnd [in]

Optional handle to a caller window. A trust provider can use this value to determine whether it can interact with the user. However, trust providers typically perform verification actions without input from the user.

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INVALID_HANDLE_VALUE"></a><a id="invalid_handle_value"></a><dl>
<dt><b>INVALID_HANDLE_VALUE</b></dt>
</dl>
</td>
<td width="60%">
There is no interactive user. The trust provider performs the verification action without the user's assistance.

</td>
</tr>
<tr>
<td width="40%"><a id="Zero"></a><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
The trust provider can use the interactive desktop to display its user interface.

</td>
</tr>
<tr>
<td width="40%"><a id="A_valid_window_handle"></a><a id="a_valid_window_handle"></a><a id="A_VALID_WINDOW_HANDLE"></a><dl>
<dt><b>A valid window handle</b></dt>
</dl>
</td>
<td width="60%">
A trust provider can treat any value other than INVALID_HANDLE_VALUE or zero as a valid window handle that it can use to interact with the user.

</td>
</tr>
</table>

### -param pgActionID [in]

A pointer to a <b>GUID</b> structure that identifies an action and the <a href="/windows/desktop/SecGloss/t-gly">trust provider</a> that supports that action. This value indicates the type of verification action to be performed on the structure pointed to by <i>pWinTrustData</i>.

The WinTrust service is designed to work with trust providers implemented by third parties. Each trust provider provides its own unique set of action identifiers. For information about the action identifiers supported by a trust provider, see the documentation for that trust provider.

For example, Microsoft provides a Software Publisher Trust Provider that can establish the trustworthiness of software being downloaded from the Internet or some other public network. The Software Publisher Trust Provider supports the following action identifiers. These constants are defined in Softpub.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DRIVER_ACTION_VERIFY"></a><a id="driver_action_verify"></a><dl>
<dt><b>DRIVER_ACTION_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Verify the
authenticity of a Windows Hardware Quality Labs (WHQL) signed driver.  This is an Authenticode add-on
policy provider.

</td>
</tr>
<tr>
<td width="40%"><a id="HTTPSPROV_ACTION"></a><a id="httpsprov_action"></a><dl>
<dt><b>HTTPSPROV_ACTION</b></dt>
</dl>
</td>
<td width="60%">
Verify an SSL/TLS connection established by WinINet.

</td>
</tr>
<tr>
<td width="40%"><a id="OFFICESIGN_ACTION_VERIFY"></a><a id="officesign_action_verify"></a><dl>
<dt><b>OFFICESIGN_ACTION_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
 This Action ID is not supported. Verify the
authenticity of a structured storage file by using the Microsoft Office
Authenticode add-on policy provider.

<b>Windows Server 2003 and Windows XP:  </b>This Action ID is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="WINTRUST_ACTION_GENERIC_CHAIN_VERIFY"></a><a id="wintrust_action_generic_chain_verify"></a><dl>
<dt><b>WINTRUST_ACTION_GENERIC_CHAIN_VERIFY</b></dt>
</dl>
</td>
<td width="60%">
Verify
certificate chains created from any object type.
A callback is provided to implement the final chain policy by using
the chain context for each signer and counter signer.

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
<td width="40%"><a id="WINTRUST_ACTION_TRUSTPROVIDER_TEST"></a><a id="wintrust_action_trustprovider_test"></a><dl>
<dt><b>WINTRUST_ACTION_TRUSTPROVIDER_TEST</b></dt>
</dl>
</td>
<td width="60%">
Write
the <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_data">CRYPT_PROVIDER_DATA</a> structure to a file after calling the
Authenticode policy provider.

</td>
</tr>
</table>

### -param pWVTData [in]

A pointer that, when cast as a 
<a href="/windows/desktop/api/wintrust/ns-wintrust-wintrust_data">WINTRUST_DATA</a> structure, contains information that the <a href="/windows/desktop/SecGloss/t-gly">trust provider</a> needs to process the specified action identifier. Typically, the structure includes information that identifies the object that the trust provider must evaluate.

The format of the structure depends on the action identifier. For information about the data required for a specific action identifier, see the documentation for the trust provider that supports that action.

## -returns

If the trust provider verifies that the subject is trusted for the specified action, the return value is zero.  No other value besides zero should be considered a successful return.

If the trust provider does not verify that the subject is trusted for the specified action, the function returns a status code from the <a href="/windows/desktop/SecGloss/t-gly">trust provider</a>.<div class="alert"><b>Note</b>  The return value is a <b>LONG</b>, not an <b>HRESULT</b> as previously documented. Do not use <b>HRESULT</b> macros such as <b>SUCCEEDED</b> to determine whether the function succeeded. Instead, check the return value for equality to zero.</div>
<div> </div>


For example, a trust provider might indicate that the subject is not trusted, or is trusted but with limitations or warnings. The return value can be a trust-provider-specific value described in the documentation for an individual trust provider, or it can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_SUBJECT_NOT_TRUSTED</b></dt>
</dl>
</td>
<td width="60%">
The subject failed the specified verification action. Most trust providers return a more detailed error code that describes the reason for the failure.

<div class="alert"><b>Note</b>  <p class="note">The <b>TRUST_E_SUBJECT_NOT_TRUSTED</b> return code may be returned depending on the value of the <b>EnableCertPaddingCheck</b> registry key under <b>HKLM\Software\Microsoft\Cryptography\Wintrust\Config</b>. If <b>EnableCertPaddingCheck</b> is set to "1", then an additional check is performed to verify that the <b>WIN_CERTIFICATE</b> structure does not contain extraneous information. The check validates that there is no non-zero data beyond the PKCS #7 structure.  For more information, please refer to the following security advisory: <a href="/security-updates/SecurityAdvisories/2014/2915720">http://technet.microsoft.com/security/advisory/2915720#section1</a>.

</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_PROVIDER_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The trust provider is not recognized on this system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_ACTION_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The trust provider does not support the specified action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUST_E_SUBJECT_FORM_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The trust provider does not support the form specified for the subject.

</td>
</tr>
</table>

## -remarks

The <b>WinVerifyTrust</b> function enables applications to invoke a <a href="/windows/desktop/SecGloss/t-gly">trust provider</a> to verify that a specified object satisfies the criteria of a specified verification operation. The <i>pgActionID</i> parameter identifies the verification operation, and the <i>pWinTrustData</i> parameter identifies the object whose trust is to be verified. A trust provider is a DLL registered with the operating system. A call to <b>WinVerifyTrust</b> forwards that call to the registered trust provider, if there is one, that supports that specified action identifier.

For example, the Software Publisher Trust Provider can verify that an executable image file comes from a trusted software publisher and that the code in the file has not been modified since it was signed. In this case, the <i>pWinTrustData</i> parameter specifies the name of the file and the type of file, such as a Microsoft <a href="/windows/desktop/SecGloss/p-gly">Portable Executable</a> image file.

Each trust provider supports a specific set of actions that it can evaluate. Each action has a GUID that identifies it. A trust provider can support any number of action identifiers, but two trust providers cannot support the same action identifier.

For an example that demonstrates how to use this function to verify the signature of a portable executable (PE) file, see <a href="/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file">Example C Program: Verifying the Signature of a PE File</a>.
