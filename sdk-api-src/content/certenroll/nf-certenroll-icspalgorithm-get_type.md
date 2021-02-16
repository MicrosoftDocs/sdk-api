---
UID: NF:certenroll.ICspAlgorithm.get_Type
title: ICspAlgorithm::get_Type (certenroll.h)
description: Retrieves the algorithm type.
helpviewer_keywords: ["ICspAlgorithm interface [Security]","Type property","ICspAlgorithm.Type","ICspAlgorithm.get_Type","ICspAlgorithm::Type","ICspAlgorithm::get_Type","Type property [Security]","Type property [Security]","ICspAlgorithm interface","XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE","XCN_BCRYPT_CIPHER_INTERFACE","XCN_BCRYPT_HASH_INTERFACE","XCN_BCRYPT_RNG_INTERFACE","XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE","XCN_BCRYPT_SIGNATURE_INTERFACE","XCN_BCRYPT_UNKNOWN_INTERFACE","certenroll/ICspAlgorithm::Type","certenroll/ICspAlgorithm::get_Type","get_Type","security.icspalgorithm_type_property"]
old-location: security\icspalgorithm_type_property.htm
tech.root: security
ms.assetid: 28bffe60-10f2-462e-8067-943b12285982
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],Type property, ICspAlgorithm.Type, ICspAlgorithm.get_Type, ICspAlgorithm::Type, ICspAlgorithm::get_Type, Type property [Security], Type property [Security],ICspAlgorithm interface, XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, XCN_BCRYPT_CIPHER_INTERFACE, XCN_BCRYPT_HASH_INTERFACE, XCN_BCRYPT_RNG_INTERFACE, XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, XCN_BCRYPT_SIGNATURE_INTERFACE, XCN_BCRYPT_UNKNOWN_INTERFACE, certenroll/ICspAlgorithm::Type, certenroll/ICspAlgorithm::get_Type, get_Type, security.icspalgorithm_type_property
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
 - ICspAlgorithm::get_Type
 - certenroll/ICspAlgorithm::get_Type
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
 - ICspAlgorithm.Type
 - ICspAlgorithm.get_Type
---

# ICspAlgorithm::get_Type


## -description

The <b>Type</b> property retrieves the algorithm type. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The main difference between the <b>Type</b> property and the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_operations">Operations</a> property is that the latter contains a bitfield in which multiple bits can be set. Because many algorithms can be used for multiple purposes, the <b>Operations</b> property is often more useful. The <b>Type</b> value can correspond to only one of the <b>Operations</b> value bits. For example, if the <b>Operations</b> property returns XCN_NCRYPT_SIGNATURE_OPERATION | XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, the <b>Type</b> property may return XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_operations">Operations</a>