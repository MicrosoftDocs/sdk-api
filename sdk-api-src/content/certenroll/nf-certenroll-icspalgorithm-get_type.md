---
UID: NF:certenroll.ICspAlgorithm.get_Type
title: ICspAlgorithm::get_Type (certenroll.h)
author: windows-sdk-content
description: Retrieves the algorithm type.
old-location: security\icspalgorithm_type_property.htm
tech.root: seccertenroll
ms.assetid: 28bffe60-10f2-462e-8067-943b12285982
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],Type property, ICspAlgorithm.Type, ICspAlgorithm.get_Type, ICspAlgorithm::Type, ICspAlgorithm::get_Type, Type property [Security], Type property [Security],ICspAlgorithm interface, XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE, XCN_BCRYPT_CIPHER_INTERFACE, XCN_BCRYPT_HASH_INTERFACE, XCN_BCRYPT_RNG_INTERFACE, XCN_BCRYPT_SECRET_AGREEMENT_INTERFACE, XCN_BCRYPT_SIGNATURE_INTERFACE, XCN_BCRYPT_UNKNOWN_INTERFACE, certenroll/ICspAlgorithm::Type, certenroll/ICspAlgorithm::get_Type, get_Type, security.icspalgorithm_type_property
ms.topic: method
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
 - ICspAlgorithm.Type
 - ICspAlgorithm.get_Type
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspAlgorithm::get_Type


## -description


The <b>Type</b> property retrieves the algorithm type. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The main difference between the <b>Type</b> property and the <a href="https://msdn.microsoft.com/46e6bf91-a50a-4360-9bfe-e41e8bcc1112">Operations</a> property is that the latter contains a bitfield in which multiple bits can be set. Because many algorithms can be used for multiple purposes, the <b>Operations</b> property is often more useful. The <b>Type</b> value can correspond to only one of the <b>Operations</b> value bits. For example, if the <b>Operations</b> property returns XCN_NCRYPT_SIGNATURE_OPERATION | XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, the <b>Type</b> property may return XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE.




## -see-also




<a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/46e6bf91-a50a-4360-9bfe-e41e8bcc1112">Operations</a>
 

 

