---
UID: NF:certenroll.ICspAlgorithm.get_Operations
title: ICspAlgorithm::get_Operations
author: windows-sdk-content
description: Retrieves the operations that can be performed by the algorithm.
old-location: security\icspalgorithm_operations.htm
old-project: seccertenroll
ms.assetid: 46e6bf91-a50a-4360-9bfe-e41e8bcc1112
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICspAlgorithm interface [Security],Operations property, ICspAlgorithm.Operations, ICspAlgorithm.get_Operations, ICspAlgorithm::Operations, ICspAlgorithm::get_Operations, Operations property [Security], Operations property [Security],ICspAlgorithm interface, XCN_NCRYPT_ANY_ASYMMETRIC_OPERATION, XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, XCN_NCRYPT_CIPHER_OPERATION, XCN_NCRYPT_HASH_OPERATION, XCN_NCRYPT_RNG_OPERATION, XCN_NCRYPT_SECRET_AGREEMENT_OPERATION, XCN_NCRYPT_SIGNATURE_OPERATION, certenroll/ICspAlgorithm::Operations, certenroll/ICspAlgorithm::get_Operations, get_Operations, security.icspalgorithm_operations
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspAlgorithm::get_Operations


## -description


The <b>Operations</b> property retrieves the operations that can be performed by the algorithm. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The main difference between the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property and the <b>Operations</b> property is that the latter contains a bitfield in which multiple bits can be set. Because many algorithms can be used for multiple purposes, the <b>Operations</b> property is often more useful. The <b>Type</b> value can correspond to only one of the <b>Operations</b> value bits. For example, if the <b>Operations</b> property returns XCN_NCRYPT_SIGNATURE_OPERATION | XCN_NCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, the <b>Type</b> property may return XCN_BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE.




## -see-also




<a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>
 

 

