---
UID: NF:certenroll.ICspAlgorithm.GetAlgorithmOid
title: ICspAlgorithm::GetAlgorithmOid (certenroll.h)
description: Retrieves the algorithm object identifier (OID). This method is web enabled.
helpviewer_keywords: ["GetAlgorithmOid","GetAlgorithmOid method [Security]","GetAlgorithmOid method [Security]","ICspAlgorithm interface","ICspAlgorithm interface [Security]","GetAlgorithmOid method","ICspAlgorithm.GetAlgorithmOid","ICspAlgorithm::GetAlgorithmOid","certenroll/ICspAlgorithm::GetAlgorithmOid","security.icspalgorithm_getalgorithmoid_method"]
old-location: security\icspalgorithm_getalgorithmoid_method.htm
tech.root: security
ms.assetid: b922154d-0d57-4473-b331-c0082d9e5db5
ms.date: 12/05/2018
ms.keywords: GetAlgorithmOid, GetAlgorithmOid method [Security], GetAlgorithmOid method [Security],ICspAlgorithm interface, ICspAlgorithm interface [Security],GetAlgorithmOid method, ICspAlgorithm.GetAlgorithmOid, ICspAlgorithm::GetAlgorithmOid, certenroll/ICspAlgorithm::GetAlgorithmOid, security.icspalgorithm_getalgorithmoid_method
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
 - ICspAlgorithm::GetAlgorithmOid
 - certenroll/ICspAlgorithm::GetAlgorithmOid
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
 - ICspAlgorithm.GetAlgorithmOid
---

# ICspAlgorithm::GetAlgorithmOid


## -description

The <b>GetAlgorithmOid</b> method retrieves the  algorithm object identifier (OID). This method is web enabled.

## -parameters

### -param Length [in]

A <b>LONG</b> variable that identifies the required key size of the symmetric encryption algorithm. Use this parameter to retrieve a specific AES algorithm from a Cryptography API: Next Generation (CNG) key storage provider (KSP). A KSP may list only one algorithm named AES but support all of the AES variants in the following list:<ul>
<li>szOID_NIST_AES128_CBC (2.16.840.1.101.3.4.1.2)</li>
<li>szOID_NIST_AES192_CBC (2.16.840.1.101.3.4.1.22)</li>
<li>szOID_NIST_AES256_CBC (2.16.840.1.101.3.4.1.42)</li>
<li>szOID_NIST_AES128_WRAP (2.16.840.1.101.3.4.1.5)</li>
<li>szOID_NIST_AES192_WRAP (2.16.840.1.101.3.4.1.25)</li>
<li>szOID_NIST_AES256_WRAP (2.16.840.1.101.3.4.1.45)</li>
</ul>


 If you specify zero for the <i>Length</i> parameter and <b>AlgorithmFlagsNone</b> (0x00000000) for the  <i>AlgFlags</i> parameter, the OID associated with the default algorithm is retrieved. For the Microsoft Software KSP and the Microsoft Smart Card KSP, the default AES algorithm is szOID_NIST_AES128_CBC (2.16.840.1.101.3.4.1.2).<div class="alert"><b>Note</b>  This parameter must be zero for any algorithm other than a symmetric encryption algorithm.</div>
<div> </div>

### -param AlgFlags [in]

An  <a href="/windows/desktop/api/certenroll/ne-certenroll-algorithmflags">AlgorithmFlags</a> enumeration value that specifies whether to search for a key wrapping algorithm. This can be one of the following values:<ul>
<li><b>AlgorithmFlagsNone</b></li>
<li><b>AlgorithmFlagsWrap</b></li>
</ul>


Specifying <b>AlgorithmFlagsWrap</b> causes this method to search for algorithms for which the display name ends with "wrap". This includes the following OIDs:<ul>
<li>szOID_NIST_AES128_WRAP (2.16.840.1.101.3.4.1.5)</li>
<li>szOID_NIST_AES192_WRAP (2.16.840.1.101.3.4.1.25)</li>
<li>szOID_NIST_AES256_WRAP (2.16.840.1.101.3.4.1.45)</li>
<li>XCN_OID_RSA_SMIMEalgCMS3DESwrap   (1.2.840.113549.1.9.16.3.6)</li>
<li>XCN_OID_RSA_SMIMEalgCMSRC2wrap    (1.2.840.113549.1.9.16.3.7)</li>
</ul>


 If you specify zero for the <i>Length</i> parameter and <b>AlgorithmFlagsNone</b> (0x00000000) for the  <i>AlgFlags</i> parameter, the OID associated with the default algorithm is retrieved. For the Microsoft Software KSP and the Microsoft Smart Card KSP, the default AES algorithm is szOID_NIST_AES128_CBC (2.16.840.1.101.3.4.1.2).<div class="alert"><b>Note</b>  This parameter must be zero for any algorithm other than a symmetric encryption algorithm.</div>
<div> </div>

### -param ppValue [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface that represents the algorithm OID.

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
The algorithm OID could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The CSP information has not been initialized. For more information, see the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface.

</td>
</tr>
</table>

## -remarks

You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromname">InitializeFromName</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromtype">InitializeFromType</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface before calling <b>GetAlgorithmOid</b>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>