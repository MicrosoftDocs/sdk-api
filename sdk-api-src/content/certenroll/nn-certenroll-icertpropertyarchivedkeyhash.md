---
UID: NN:certenroll.ICertPropertyArchivedKeyHash
title: ICertPropertyArchivedKeyHash (certenroll.h)
description: Represents a SHA-1 hash of an encrypted private key submitted to a certification authority for archival.
old-location: security\icertpropertyarchivedkeyhash.htm
tech.root: seccertenroll
ms.assetid: 06696346-b9d1-4229-991e-539862cff3c9
ms.date: 12/05/2018
ms.keywords: ICertPropertyArchivedKeyHash, ICertPropertyArchivedKeyHash interface [Security], ICertPropertyArchivedKeyHash interface [Security],described, certenroll/ICertPropertyArchivedKeyHash, security.icertpropertyarchivedkeyhash
ms.topic: interface
f1_keywords:
- certenroll/ICertPropertyArchivedKeyHash
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
- ICertPropertyArchivedKeyHash
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertPropertyArchivedKeyHash interface


## -description


The <b>ICertPropertyArchivedKeyHash</b> interface represents a SHA-1 hash of an encrypted private key submitted to a certification authority for archival.

To archive a private key, a client first encrypts the key by using the public key from a CA exchange certificate. The client then places the encrypted private key into a PKCS #7 EnvelopedData structure and hashes the structure by using a SHA-1 hash algorithm. The resulting hash  is used to initialize an <b>ICertPropertyArchivedKeyHash</b> object and is included in a CMC certificate request. The property value is typically associated with the certificate after the certificate response is received from the CA and before the response is placed in a store.

This property is initialized by the enrollment process and associated with the dummy certificate that is temporarily copied to the request store. If the CA denies the certificate request, the dummy certificate in the request store and all properties associated with it are deleted. If the CA issues the certificate and it is installed in the certificate store, this property is associated with the new certificate in the personal store and the dummy certificate is deleted.<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_ARCHIVED_KEY_HASH_PROP_IDD.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyArchivedKeyHash</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyArchivedKeyHash</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertPropertyArchivedKeyHash</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyarchivedkeyhash-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object from a  byte array that contains the hash.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertPropertyArchivedKeyHash</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertpropertyarchivedkeyhash-get_archivedkeyhash">ArchivedKeyHash</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a SHA-1 hash of the private key.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
 

 

