---
UID: NN:certenroll.ICertPropertyArchivedKeyHash
title: ICertPropertyArchivedKeyHash (certenroll.h)
description: Represents a SHA-1 hash of an encrypted private key submitted to a certification authority for archival.
helpviewer_keywords: ["ICertPropertyArchivedKeyHash","ICertPropertyArchivedKeyHash interface [Security]","ICertPropertyArchivedKeyHash interface [Security]","described","certenroll/ICertPropertyArchivedKeyHash","security.icertpropertyarchivedkeyhash"]
old-location: security\icertpropertyarchivedkeyhash.htm
tech.root: security
ms.assetid: 06696346-b9d1-4229-991e-539862cff3c9
ms.date: 12/05/2018
ms.keywords: ICertPropertyArchivedKeyHash, ICertPropertyArchivedKeyHash interface [Security], ICertPropertyArchivedKeyHash interface [Security],described, certenroll/ICertPropertyArchivedKeyHash, security.icertpropertyarchivedkeyhash
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
 - ICertPropertyArchivedKeyHash
 - certenroll/ICertPropertyArchivedKeyHash
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
 - ICertPropertyArchivedKeyHash
---

# ICertPropertyArchivedKeyHash interface


## -description

The <b>ICertPropertyArchivedKeyHash</b> interface represents a SHA-1 hash of an encrypted private key submitted to a certification authority for archival.

To archive a private key, a client first encrypts the key by using the public key from a CA exchange certificate. The client then places the encrypted private key into a PKCS #7 EnvelopedData structure and hashes the structure by using a SHA-1 hash algorithm. The resulting hash  is used to initialize an <b>ICertPropertyArchivedKeyHash</b> object and is included in a CMC certificate request. The property value is typically associated with the certificate after the certificate response is received from the CA and before the response is placed in a store.

This property is initialized by the enrollment process and associated with the dummy certificate that is temporarily copied to the request store. If the CA denies the certificate request, the dummy certificate in the request store and all properties associated with it are deleted. If the CA issues the certificate and it is installed in the certificate store, this property is associated with the new certificate in the personal store and the dummy certificate is deleted.<div class="alert"><b>Note</b>  The <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> value is XCN_CERT_ARCHIVED_KEY_HASH_PROP_IDD.</div>
<div> </div>

## -inheritance

The <b>ICertPropertyArchivedKeyHash</b> interface inherits from <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>. <b>ICertPropertyArchivedKeyHash</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
