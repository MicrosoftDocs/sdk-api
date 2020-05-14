---
UID: NF:certenroll.ICspAlgorithm.get_LongName
title: ICspAlgorithm::get_LongName (certenroll.h)
description: Retrieves the full name of the algorithm.helpviewer_keywords: ["ICspAlgorithm interface [Security]","LongName property","ICspAlgorithm.LongName","ICspAlgorithm.get_LongName","ICspAlgorithm::LongName","ICspAlgorithm::get_LongName","LongName property [Security]","LongName property [Security]","ICspAlgorithm interface","certenroll/ICspAlgorithm::LongName","certenroll/ICspAlgorithm::get_LongName","get_LongName","security.icspalgorithm_longname_property"]
old-location: security\icspalgorithm_longname_property.htm
tech.root: seccertenroll
ms.assetid: aaa5175f-c110-4e76-9145-1c667ea169a1
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],LongName property, ICspAlgorithm.LongName, ICspAlgorithm.get_LongName, ICspAlgorithm::LongName, ICspAlgorithm::get_LongName, LongName property [Security], LongName property [Security],ICspAlgorithm interface, certenroll/ICspAlgorithm::LongName, certenroll/ICspAlgorithm::get_LongName, get_LongName, security.icspalgorithm_longname_property
f1_keywords:
- certenroll/ICspAlgorithm.LongName
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- ICspAlgorithm.LongName
- ICspAlgorithm.get_LongName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspAlgorithm::get_LongName


## -description


The <b>LongName</b> property retrieves the full name of the algorithm.

This property is read-only.


## -parameters


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_name">Name</a> property retrieves a short algorithm name. Call the <b>LongName</b> property to retrieve a more descriptive name. The names are not localized. Examples are shown in the following table.

<div class="alert"><b>Note</b>  Cryptography API: Next Generation (CNG) key storage providers (KSPs) do not support the long name concept. The <b>LongName</b> property and <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_name">Name</a> property return an abbreviated name.</div>
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




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>
 

 

