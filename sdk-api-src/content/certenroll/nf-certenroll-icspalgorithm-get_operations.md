---
UID: NF:certenroll.ICspAlgorithm.get_Operations
title: ICspAlgorithm::get_Operations (certenroll.h)
description: Retrieves the operations that can be performed by the algorithm.
helpviewer_keywords: ["ICspAlgorithm interface [Security]","Operations property","ICspAlgorithm.Operations","ICspAlgorithm.get_Operations","ICspAlgorithm::Operations","ICspAlgorithm::get_Operations","Operations property [Security]","Operations property [Security]","ICspAlgorithm interface","XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION","XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION","XCN_NCRYPT_CIPHER_OPERATION","XCN_NCRYPT_HASH_OPERATION","XCN_NCRYPT_RNG_OPERATION","XCN_NCRYPT_SECRET_AGREEMENT_OPERATION","XCN_NCRYPT_SIGNATURE_OPERATION","certenroll/ICspAlgorithm::Operations","certenroll/ICspAlgorithm::get_Operations","get_Operations","security.icspalgorithm_operations"]
old-location: security\icspalgorithm_operations.htm
tech.root: security
ms.assetid: 46e6bf91-a50a-4360-9bfe-e41e8bcc1112
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],Operations property, ICspAlgorithm.Operations, ICspAlgorithm.get_Operations, ICspAlgorithm::Operations, ICspAlgorithm::get_Operations, Operations property [Security], Operations property [Security],ICspAlgorithm interface, XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, XCN_NCRYPT_CIPHER_OPERATION, XCN_NCRYPT_HASH_OPERATION, XCN_NCRYPT_RNG_OPERATION, XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, XCN_NCRYPT_SIGNATURE_OPERATION, certenroll/ICspAlgorithm::Operations, certenroll/ICspAlgorithm::get_Operations, get_Operations, security.icspalgorithm_operations
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
 - ICspAlgorithm::get_Operations
 - certenroll/ICspAlgorithm::get_Operations
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
 - ICspAlgorithm.Operations
 - ICspAlgorithm.get_Operations
---

# ICspAlgorithm::get_Operations


## -description

The <b>Operations</b> property retrieves the operations that can be performed by the algorithm. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The main difference between the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_type">Type</a> property and the <b>Operations</b> property is that the latter contains a bitfield in which multiple bits can be set. Because many algorithms can be used for multiple purposes, the <b>Operations</b> property is often more useful. The <b>Type</b> value can correspond to only one of the <b>Operations</b> value bits. For example, if the <b>Operations</b> property returns XCN_NCRYPT_SIGNATURE_OPERATION | XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, the <b>Type</b> property may return XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_type">Type</a>