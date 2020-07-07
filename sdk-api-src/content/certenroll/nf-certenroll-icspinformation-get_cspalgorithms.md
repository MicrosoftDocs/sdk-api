---
UID: NF:certenroll.ICspInformation.get_CspAlgorithms
title: ICspInformation::get_CspAlgorithms (certenroll.h)
description: Retrieves a collection of ICspAlgorithm interfaces that contain information about the algorithms supported by the provider.
helpviewer_keywords: ["CspAlgorithms property [Security]","CspAlgorithms property [Security]","ICspInformation interface","ICspInformation interface [Security]","CspAlgorithms property","ICspInformation.CspAlgorithms","ICspInformation.get_CspAlgorithms","ICspInformation::CspAlgorithms","ICspInformation::get_CspAlgorithms","certenroll/ICspInformation::CspAlgorithms","certenroll/ICspInformation::get_CspAlgorithms","get_CspAlgorithms","security.icspinformation_cspalgorithms_property"]
old-location: security\icspinformation_cspalgorithms_property.htm
tech.root: seccertenroll
ms.assetid: e74f1aa3-883b-40e4-8052-6651eaa4b63f
ms.date: 12/05/2018
ms.keywords: CspAlgorithms property [Security], CspAlgorithms property [Security],ICspInformation interface, ICspInformation interface [Security],CspAlgorithms property, ICspInformation.CspAlgorithms, ICspInformation.get_CspAlgorithms, ICspInformation::CspAlgorithms, ICspInformation::get_CspAlgorithms, certenroll/ICspInformation::CspAlgorithms, certenroll/ICspInformation::get_CspAlgorithms, get_CspAlgorithms, security.icspinformation_cspalgorithms_property
f1_keywords:
- certenroll/ICspInformation.CspAlgorithms
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
- ICspInformation.CspAlgorithms
- ICspInformation.get_CspAlgorithms
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICspInformation::get_CspAlgorithms


## -description


The <b>CspAlgorithms</b> property retrieves a collection of <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a> interfaces that contain information about the algorithms supported by the provider. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



An <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a> object contains information about the cryptographic algorithms supported by the provider. This includes the algorithm <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID), the permitted key lengths and incremental lengths, the algorithm name and abbreviated name, and a Boolean value that specifies whether the algorithm OID object is valid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>
 

 

