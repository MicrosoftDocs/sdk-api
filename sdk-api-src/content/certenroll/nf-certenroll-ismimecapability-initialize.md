---
UID: NF:certenroll.ISmimeCapability.Initialize
title: ISmimeCapability::Initialize (certenroll.h)
description: Initializes the object from a symmetric encryption algorithm object identifier (OID) and an optional key length.
helpviewer_keywords: ["ISmimeCapability interface [Security]","Initialize method","ISmimeCapability.Initialize","ISmimeCapability::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ISmimeCapability interface","certenroll/ISmimeCapability::Initialize","security.ismimecapability_initialize_method"]
old-location: security\ismimecapability_initialize_method.htm
tech.root: security
ms.assetid: d972121d-ecfa-4a79-9322-dd0d0b81ba68
ms.date: 12/05/2018
ms.keywords: ISmimeCapability interface [Security],Initialize method, ISmimeCapability.Initialize, ISmimeCapability::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ISmimeCapability interface, certenroll/ISmimeCapability::Initialize, security.ismimecapability_initialize_method
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
 - ISmimeCapability::Initialize
 - certenroll/ISmimeCapability::Initialize
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
 - ISmimeCapability.Initialize
---

# ISmimeCapability::Initialize


## -description

The <b>Initialize</b> method initializes the object from a symmetric encryption algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and an optional key length.

## -parameters

### -param pObjectId [in]

Pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents the OID.

### -param BitCount [in]

A <b>LONG</b> variable that contains the bit length of the symmetric key.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> pointer is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The following symmetric encryption algorithms are supported by the Certificate Enrollment API. Only the <a href="/windows/desktop/SecGloss/r-gly">RC2</a> and <a href="/windows/desktop/SecGloss/r-gly">RC4</a> algorithms have variable key lengths that can be specified.<table>
<tr>
<th>OID</th>
<th>Key length</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_OIWSEC_desCBC1.3.14.3.2.7

</td>
<td>56</td>
<td>The key size is of the DES CBC algorithm is 56 bits. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_RSA_DES_EDE3_CBC1.2.840.113549.3.7

</td>
<td>168</td>
<td>The key size is of the 3DES CBC algorithm is 168 bits. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC2CBC1.2.840.113549.3.2

</td>
<td>40 to 128</td>
<td>RC4 is a variable key algorithm. common values are 40, 64, and 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC41.2.840.113549.3.4

</td>
<td>40 to 128</td>
<td>RC4 is a variable key algorithm. common values are 40, 64, and 128 bits.</td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMS3DESwrap1.2.840.113549.1.9.16.3.6

</td>
<td>168</td>
<td>The key size of the MMS <a href="/windows/desktop/SecGloss/d-gly">Data Encryption Standard</a> (DES) key wrap algorithm is 168 bits. You do not need to specify this value. </td>
</tr>
<tr>
<td>XCN_OID_RSA_SMIMEalgCMSRC2wrap1.2.840.113549.1.9.16.3.7

</td>
<td>128</td>
<td>The key size of the MMS RC2 key wrap algorithm is 128 bits. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_CBC2.16.840.1.101.3.4.1.2

</td>
<td>128</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_CBC2.16.840.1.101.3.4.1.22

</td>
<td>192</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_CBC2.16.840.1.101.3.4.1.42

</td>
<td>256</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES128_WRAP2.16.840.1.101.3.4.1.5

</td>
<td>128</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES192_WRAP2.16.840.1.101.3.4.1.25

</td>
<td>192</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
<tr>
<td>XCN_OID_NIST_AES256_WRAP2.16.840.1.101.3.4.1.45

</td>
<td>256</td>
<td>The key size is implied by the OID. You do not need to specify this value.</td>
</tr>
</table>
 



The key length that you specify for RC2 and RC4 algorithms must be consistent with that supported by the cryptographic provider or providers used by the client. For more information, see <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>. You can retrieve the bit length by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ismimecapability-get_bitcount">BitCount</a> property,  and you can retrieve the algorithm OID by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ismimecapability-get_objectid">ObjectId</a> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapabilities">ISmimeCapabilities</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>