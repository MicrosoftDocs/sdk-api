---
UID: NF:certenroll.IX509PrivateKey.Verify
title: IX509PrivateKey::Verify (certenroll.h)
description: Verifies that a private key exists and can be used by the client but does not open the key.
helpviewer_keywords: ["IX509PrivateKey interface [Security]","Verify method","IX509PrivateKey.Verify","IX509PrivateKey::Verify","Verify","Verify method [Security]","Verify method [Security]","IX509PrivateKey interface","VerifyAllowUI","VerifyNone","VerifySilent","VerifySmartCardNone","VerifySmartCardSilent","certenroll/IX509PrivateKey::Verify","security.ix509privatekey_verify"]
old-location: security\ix509privatekey_verify.htm
tech.root: security
ms.assetid: 4a792c39-71a7-4289-854d-98e6f749a526
ms.date: 12/05/2018
ms.keywords: IX509PrivateKey interface [Security],Verify method, IX509PrivateKey.Verify, IX509PrivateKey::Verify, Verify, Verify method [Security], Verify method [Security],IX509PrivateKey interface, VerifyAllowUI, VerifyNone, VerifySilent, VerifySmartCardNone, VerifySmartCardSilent, certenroll/IX509PrivateKey::Verify, security.ix509privatekey_verify
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509PrivateKey::Verify
 - certenroll/IX509PrivateKey::Verify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.Verify
---

# IX509PrivateKey::Verify


## -description

The <b>Verify</b> method verifies that a private key exists and can be used by the client but does not open the key.

## -parameters

### -param VerifyType [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-x509privatekeyverify">X509PrivateKeyVerify</a> enumeration value that specifies execution options for the method. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VerifyNone"></a><a id="verifynone"></a><a id="VERIFYNONE"></a><dl>
<dt><b>VerifyNone</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySilent"></a><a id="verifysilent"></a><a id="VERIFYSILENT"></a><dl>
<dt><b>VerifySilent</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify if a user interface is required to open the private key; otherwise verification occurs. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySmartCardNone"></a><a id="verifysmartcardnone"></a><a id="VERIFYSMARTCARDNONE"></a><dl>
<dt><b>VerifySmartCardNone</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify if the key is stored on a smart card; otherwise, this value is equivalent to  <b>VerifyAllowUI</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifySmartCardSilent"></a><a id="verifysmartcardsilent"></a><a id="VERIFYSMARTCARDSILENT"></a><dl>
<dt><b>VerifySmartCardSilent</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Does not verify if a user interface is required to open the private key and the key is stored on a smart card;  otherwise, this value is equivalent to   <b>VerifyAllowUI</b>. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="VerifyAllowUI"></a><a id="verifyallowui"></a><a id="VERIFYALLOWUI"></a><dl>
<dt><b>VerifyAllowUI</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The method allows a user interface to be displayed.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. Also, this method calls the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetuserkey">CryptGetUserKey</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> CryptoAPI functions and can return errors identified in that documentation. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
Properties related to the CSP or KSP could not be found.

</td>
</tr>
</table>

## -remarks

If <b>VerifySilent</b> or <b>VerifySmartCardSilent</b> values are set and the cryptographic provider specifies that a user interface is necessary, the key will not be opened, but the method returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509privatekey">IX509PrivateKey</a>