---
UID: NS:wincrypt._CTL_ANY_SUBJECT_INFO
title: "_CTL_ANY_SUBJECT_INFO"
author: windows-driver-content
description: Contains a SubjectAlgorithm to be matched in the certificate trust list (CTL) and the SubjectIdentifier to be matched in one of the CTL entries in calls to CertFindSubjectInCTL.
old-location: security\ctl_any_subject_info.htm
old-project: SecCrypto
ms.assetid: 367e9914-b69b-47ad-a20a-3dd067708787
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PCTL_ANY_SUBJECT_INFO, CTL_ANY_SUBJECT_INFO, CTL_ANY_SUBJECT_INFO structure [Security], PCTL_ANY_SUBJECT_INFO, PCTL_ANY_SUBJECT_INFO structure pointer [Security], _CTL_ANY_SUBJECT_INFO, _crypto2_ctl_any_subject_info, security.ctl_any_subject_info, wincrypt/CTL_ANY_SUBJECT_INFO, wincrypt/PCTL_ANY_SUBJECT_INFO"
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
req.typenames: CTL_ANY_SUBJECT_INFO, *PCTL_ANY_SUBJECT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CTL_ANY_SUBJECT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CTL_ANY_SUBJECT_INFO structure


## -description


The <b>CTL_ANY_SUBJECT_INFO</b> structure contains a <b>SubjectAlgorithm</b> to be matched in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL) and the <b>SubjectIdentifier</b> to be matched in one of the CTL entries in calls to 
<a href="https://msdn.microsoft.com/e0c81531-e649-45bb-bafe-bced00c7b16a">CertFindSubjectInCTL</a>.


## -struct-fields




### -field SubjectAlgorithm


<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure containing the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of an algorithm type and any associated additional parameters. The <b>pszObjId</b> can be set to <b>NULL</b> to exclude a <b>SubjectAlgorithm</b> comparison.


### -field SubjectIdentifier

<a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> containing a unique identifier of the subject.


## -see-also




<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/b3a63010-9025-4a86-aa48-bfb6e800a07a">CTL_FIND_SUBJECT_PARA</a>



<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>



<a href="https://msdn.microsoft.com/e0c81531-e649-45bb-bafe-bced00c7b16a">CertFindSubjectInCTL</a>
 

 

