---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICspAlgorithm::get_LongName


## -description


The <b>LongName</b> property retrieves the full name of the algorithm.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property retrieves a short algorithm name. Call the <b>LongName</b> property to retrieve a more descriptive name. The names are not localized. Examples are shown in the following table.

<div class="alert"><b>Note</b>  Cryptography API: Next Generation (CNG) key storage providers (KSPs) do not support the long name concept. The <b>LongName</b> property and <a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a> property return an abbreviated name.</div>
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




<a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a>
 

 

