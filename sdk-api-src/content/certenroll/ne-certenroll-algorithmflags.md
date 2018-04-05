---
UID: NE:certenroll.AlgorithmFlags
title: AlgorithmFlags
author: windows-driver-content
description: Contains flags that can be used to refine the search for a cryptographic algorithm.
old-location: security\algorithmflags_enum.htm
old-project: SecCertEnroll
ms.assetid: 0f067687-ae92-4500-af19-80f537620bb9
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AlgorithmFlags, AlgorithmFlags enumeration [Security], AlgorithmFlagsNone, AlgorithmFlagsWrap, certenroll/AlgorithmFlags, certenroll/AlgorithmFlagsNone, certenroll/AlgorithmFlagsWrap, security.algorithmflags_enum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: AlgorithmFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	AlgorithmFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# AlgorithmFlags enumeration


## -description


The <b>AlgorithmFlags</b> enumeration type contains flags that can be used to refine the search for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic algorithm</a>. The only flag currently defined enables retrieval of key wrapping algorithms. This enumeration is used by the <a href="https://msdn.microsoft.com/ba8c1f11-9380-43a9-b444-b0fff114a176">InitializeFromAlgorithmName</a> method on the <a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a> interface.


## -enum-fields




### -field AlgorithmFlagsNone

No flags are specified.


### -field AlgorithmFlagsWrap

The algorithm is used for key wrapping. For more information, see <a href="https://msdn.microsoft.com/ba8c1f11-9380-43a9-b444-b0fff114a176">InitializeFromAlgorithmName</a>.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/bc6608e3-cae7-4992-b599-06bc04cc8ad7">IObjectId</a>
 

 

