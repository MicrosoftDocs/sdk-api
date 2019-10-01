---
UID: NE:certenroll.AlgorithmFlags
title: AlgorithmFlags (certenroll.h)
author: windows-sdk-content
description: Contains flags that can be used to refine the search for a cryptographic algorithm.
old-location: security\algorithmflags_enum.htm
tech.root: seccertenroll
ms.assetid: 0f067687-ae92-4500-af19-80f537620bb9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AlgorithmFlags, AlgorithmFlags enumeration [Security], AlgorithmFlagsNone, AlgorithmFlagsWrap, certenroll/AlgorithmFlags, certenroll/AlgorithmFlagsNone, certenroll/AlgorithmFlagsWrap, security.algorithmflags_enum
ms.topic: enum
f1_keywords: 
 - "certenroll/AlgorithmFlags"
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - AlgorithmFlags
targetos: Windows
req.typenames: AlgorithmFlags
req.redist: 
ms.custom: 19H1
---

# AlgorithmFlags enumeration


## -description


The <b>AlgorithmFlags</b> enumeration type contains flags that can be used to refine the search for a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic algorithm</a>. The only flag currently defined enables retrieval of key wrapping algorithms. This enumeration is used by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a> method on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> interface.


## -enum-fields




### -field AlgorithmFlagsNone

No flags are specified.


### -field AlgorithmFlagsWrap

The algorithm is used for key wrapping. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a>
 

 

