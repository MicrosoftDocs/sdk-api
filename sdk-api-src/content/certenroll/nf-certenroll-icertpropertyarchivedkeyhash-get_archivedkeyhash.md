---
UID: NF:certenroll.ICertPropertyArchivedKeyHash.get_ArchivedKeyHash
title: ICertPropertyArchivedKeyHash::get_ArchivedKeyHash (certenroll.h)
description: Retrieves a SHA-1 hash of the private key.
helpviewer_keywords: ["ArchivedKeyHash property [Security]","ArchivedKeyHash property [Security]","ICertPropertyArchivedKeyHash interface","ICertPropertyArchivedKeyHash interface [Security]","ArchivedKeyHash property","ICertPropertyArchivedKeyHash.ArchivedKeyHash","ICertPropertyArchivedKeyHash.get_ArchivedKeyHash","ICertPropertyArchivedKeyHash::ArchivedKeyHash","ICertPropertyArchivedKeyHash::get_ArchivedKeyHash","certenroll/ICertPropertyArchivedKeyHash::ArchivedKeyHash","certenroll/ICertPropertyArchivedKeyHash::get_ArchivedKeyHash","get_ArchivedKeyHash","security.icertpropertyarchivedkeyhash_archivedkeyhash"]
old-location: security\icertpropertyarchivedkeyhash_archivedkeyhash.htm
tech.root: security
ms.assetid: b5f38bfc-58aa-42c6-a457-44bdfd013ce7
ms.date: 12/05/2018
ms.keywords: ArchivedKeyHash property [Security], ArchivedKeyHash property [Security],ICertPropertyArchivedKeyHash interface, ICertPropertyArchivedKeyHash interface [Security],ArchivedKeyHash property, ICertPropertyArchivedKeyHash.ArchivedKeyHash, ICertPropertyArchivedKeyHash.get_ArchivedKeyHash, ICertPropertyArchivedKeyHash::ArchivedKeyHash, ICertPropertyArchivedKeyHash::get_ArchivedKeyHash, certenroll/ICertPropertyArchivedKeyHash::ArchivedKeyHash, certenroll/ICertPropertyArchivedKeyHash::get_ArchivedKeyHash, get_ArchivedKeyHash, security.icertpropertyarchivedkeyhash_archivedkeyhash
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
 - ICertPropertyArchivedKeyHash::get_ArchivedKeyHash
 - certenroll/ICertPropertyArchivedKeyHash::get_ArchivedKeyHash
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
 - ICertPropertyArchivedKeyHash.ArchivedKeyHash
 - ICertPropertyArchivedKeyHash.get_ArchivedKeyHash
---

# ICertPropertyArchivedKeyHash::get_ArchivedKeyHash


## -description

The <b>ArchivedKeyHash</b> property retrieves a SHA-1 hash of the private key.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyarchivedkeyhash-initialize">Initialize</a> method to specify the hash.

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey">ArchivePrivateKey</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchivedkeyhash">ICertPropertyArchivedKeyHash</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate">KeyArchivalCertificate</a>