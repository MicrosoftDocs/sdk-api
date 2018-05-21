---
UID: NS:wincrypt._CTL_USAGE
title: "_CTL_USAGE"
author: windows-driver-content
description: Contains an array of object identifiers (OIDs) for Certificate Trust List (CTL) extensions.
old-location: security\ctl_usage.htm
old-project: SecCrypto
ms.assetid: 70ee138a-df94-4fc4-9de5-0d8b7704b890
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PCERT_ENHKEY_USAGE, *PCTL_USAGE, CERT_ENHKEY_USAGE, CERT_ENHKEY_USAGE structure [Security], CTL_USAGE, CTL_USAGE structure [Security], PCERT_ENHKEY_USAGE, PCERT_ENHKEY_USAGE structure pointer [Security], PCTL_USAGE, PCTL_USAGE structure pointer [Security], _CTL_USAGE, _crypto2_ctl_usage, security.ctl_usage, wincrypt/CERT_ENHKEY_USAGE, wincrypt/CTL_USAGE, wincrypt/PCERT_ENHKEY_USAGE, wincrypt/PCTL_USAGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CTL_USAGE, *PCTL_USAGE, CERT_ENHKEY_USAGE, *PCERT_ENHKEY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CTL_USAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CTL_USAGE structure


## -description


The <b>CTL_USAGE</b> structure contains an array of <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) for <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Trust List</a> (CTL) extensions. <b>CTL_USAGE</b> structures are used in functions that search for CTLs for specific uses.


## -struct-fields




### -field cUsageIdentifier

Number of elements in the <b>rgpszUsageIdentifier</b> member array.


### -field rgpszUsageIdentifier

Array of object identifiers (OIDs) of CTL extensions.


## -see-also




<a href="https://msdn.microsoft.com/bb6a7013-19ec-4263-b7a2-33c79c2b5feb">CTL_FIND_USAGE_PARA</a>



<a href="https://msdn.microsoft.com/83b015b5-a650-4a81-a9f0-c3e8a9805c81">CTL_INFO</a>



<a href="https://msdn.microsoft.com/20b3fcfb-55df-46ff-80a5-70f31a3d03b2">CertFindCertificateInStore</a>



<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a>



<a href="https://msdn.microsoft.com/d87d8157-8e52-4198-bfd4-46d83d72eb13">CertVerifyCTLUsage</a>



<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>
 

 

