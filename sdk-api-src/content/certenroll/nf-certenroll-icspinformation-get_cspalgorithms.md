---
UID: NF:certenroll.ICspInformation.get_CspAlgorithms
title: ICspInformation::get_CspAlgorithms method
author: windows-driver-content
description: Retrieves a collection of ICspAlgorithm interfaces that contain information about the algorithms supported by the provider.
old-location: security\icspinformation_cspalgorithms_property.htm
old-project: SecCertEnroll
ms.assetid: e74f1aa3-883b-40e4-8052-6651eaa4b63f
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: CspAlgorithms property [Security], CspAlgorithms property [Security], ICspInformation interface, ICspInformation, ICspInformation interface [Security], CspAlgorithms property, ICspInformation.CspAlgorithms, ICspInformation::get_CspAlgorithms, certenroll/ICspInformation::CspAlgorithms, certenroll/ICspInformation::get_CspAlgorithms, get_CspAlgorithms,ICspInformation.get_CspAlgorithms, security.icspinformation_cspalgorithms_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICspInformation.CspAlgorithms
-	ICspInformation.get_CspAlgorithms
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspInformation::get_CspAlgorithms method


## -description


The <b>CspAlgorithms</b> property retrieves a collection of <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> interfaces that contain information about the algorithms supported by the provider. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



An <a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a> object contains information about the cryptographic algorithms supported by the provider. This includes the algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID), the permitted key lengths and incremental lengths, the algorithm name and abbreviated name, and a Boolean value that specifies whether the algorithm OID object is valid.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 

