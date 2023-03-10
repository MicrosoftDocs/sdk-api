---
UID: NF:certenroll.ICspAlgorithm.get_Name
title: ICspAlgorithm::get_Name (certenroll.h)
description: Retrieves the abbreviated algorithm name.
helpviewer_keywords: ["ICspAlgorithm interface [Security]","Name property","ICspAlgorithm.Name","ICspAlgorithm.get_Name","ICspAlgorithm::Name","ICspAlgorithm::get_Name","Name property [Security]","Name property [Security]","ICspAlgorithm interface","certenroll/ICspAlgorithm::Name","certenroll/ICspAlgorithm::get_Name","get_Name","security.icspalgorithm_name_property"]
old-location: security\icspalgorithm_name_property.htm
tech.root: security
ms.assetid: af7fa894-58e2-4607-9b6e-c32d4f412ddf
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],Name property, ICspAlgorithm.Name, ICspAlgorithm.get_Name, ICspAlgorithm::Name, ICspAlgorithm::get_Name, Name property [Security], Name property [Security],ICspAlgorithm interface, certenroll/ICspAlgorithm::Name, certenroll/ICspAlgorithm::get_Name, get_Name, security.icspalgorithm_name_property
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
 - ICspAlgorithm::get_Name
 - certenroll/ICspAlgorithm::get_Name
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
 - ICspAlgorithm.Name
 - ICspAlgorithm.get_Name
---

# ICspAlgorithm::get_Name


## -description

The <b>Name</b> property retrieves the abbreviated algorithm name. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The <b>Name</b> property retrieves a shortened algorithm name. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_longname">LongName</a> property to retrieve a more descriptive name. The names are not localized. Examples are shown in the following table.

<div class="alert"><b>Note</b>  Cryptography API: Next Generation (CNG) key storage providers (KSPs) do not support the long name concept. The <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_longname">LongName</a> property and <b>Name</b> property return an abbreviated name.</div>
<div> </div>
<table>
<tr>
<th>Algorithm OID</th>
<th>Name (KSP and CSP)</th>
<th>LongName (KSP)</th>
<th>LongName (CSP)</th>
</tr>
<tr>
<td>XCN_OID_OIWSEC_desCBC(1.3.14.3.2.7)

</td>
<td>DES</td>
<td>DES</td>
<td>Data Encryption Standard (DES)</td>
</tr>
<tr>
<td>XCN_OID_OIWSEC_sha1(1.3.14.3.2.26)

</td>
<td>SHA-1</td>
<td>SHA-1</td>
<td>Secure Hash Algorithm (SHA-1)</td>
</tr>
<tr>
<td>XCN_OID_RSA_MD2(1.2.840.113549.2.2)

</td>
<td>MD2</td>
<td>MD2</td>
<td>Message Digest 2 (MD2)</td>
</tr>
<tr>
<td>XCN_OID_RSA_RC2CBC(1.2.840.113549.3.2)

</td>
<td>RC2</td>
<td>RC2</td>
<td>RSA Data Security's RC2</td>
</tr>
<tr>
<td>XCN_OID_ANSI_X942_DH(1.2.840.10046.2.1)

</td>
<td>DH_KEYX</td>
<td>DH_KEYX</td>
<td>Diffie-Hellman Key Exchange Algorithm</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>