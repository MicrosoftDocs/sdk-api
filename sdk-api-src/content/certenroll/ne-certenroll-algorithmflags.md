---
UID: NE:certenroll.AlgorithmFlags
title: AlgorithmFlags
author: windows-sdk-content
description: Contains flags that can be used to refine the search for a cryptographic algorithm.
old-location: security\algorithmflags_enum.htm
old-project: seccertenroll
ms.assetid: 0f067687-ae92-4500-af19-80f537620bb9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AlgorithmFlags, AlgorithmFlags enumeration [Security], AlgorithmFlagsNone, AlgorithmFlagsWrap, certenroll/AlgorithmFlags, certenroll/AlgorithmFlagsNone, certenroll/AlgorithmFlagsWrap, security.algorithmflags_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
req.typenames: AlgorithmFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - AlgorithmFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# AlgorithmFlags enumeration


## -description


The <b>AlgorithmFlags</b> enumeration type contains flags that can be used to refine the search for a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic algorithm</a>. The only flag currently defined enables retrieval of key wrapping algorithms. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/Aa376796(v=VS.85).aspx">InitializeFromAlgorithmName</a> method on the <a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a> interface.


## -enum-fields




### -field AlgorithmFlagsNone

No flags are specified.


### -field AlgorithmFlagsWrap

The algorithm is used for key wrapping. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa376796(v=VS.85).aspx">InitializeFromAlgorithmName</a>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376784(v=VS.85).aspx">IObjectId</a>
 

 

