---
UID: NF:certenroll.ICspStatus.get_CspAlgorithm
title: ICspStatus::get_CspAlgorithm
author: windows-sdk-content
description: Retrieves an ICspAlgorithm object that contains information about an algorithm supported by the provider.
old-location: security\icspstatus_cspalgorithm.htm
tech.root: SecCertEnroll
ms.assetid: fc86ff4a-98f4-4e14-8d24-132926c9b41d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CspAlgorithm property [Security], CspAlgorithm property [Security],ICspStatus interface, ICspStatus interface [Security],CspAlgorithm property, ICspStatus.CspAlgorithm, ICspStatus.get_CspAlgorithm, ICspStatus::CspAlgorithm, ICspStatus::get_CspAlgorithm, certenroll/ICspStatus::CspAlgorithm, certenroll/ICspStatus::get_CspAlgorithm, get_CspAlgorithm, security.icspstatus_cspalgorithm
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
 - ICspStatus.CspAlgorithm
 - ICspStatus.get_CspAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspStatus::get_CspAlgorithm


## -description


The <b>CspAlgorithm</b> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a> object that contains information about an algorithm supported by the provider. This property is web enabled.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a> object includes the following information about an algorithm:<ul>
<li>The default, minimum, maximum, and incremental lengths of the key.</li>
<li>The abbreviated and long name of the algorithm.</li>
<li>The cryptographic operations that can be performed by the algorithm.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376761(v=VS.85).aspx">ICspStatuses</a>
 

 

