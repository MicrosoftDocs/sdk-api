---
UID: NS:wincrypt._CTL_FIND_USAGE_PARA
title: "_CTL_FIND_USAGE_PARA"
author: windows-driver-content
description: A member of the CTL_FIND_SUBJECT_PARA structure and it is used by CertFindCTLInStore.
old-location: security\ctl_find_usage_para.htm
old-project: SecCrypto
ms.assetid: bb6a7013-19ec-4263-b7a2-33c79c2b5feb
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PCTL_FIND_USAGE_PARA, CTL_FIND_USAGE_PARA, CTL_FIND_USAGE_PARA structure [Security], PCTL_FIND_USAGE_PARA, PCTL_FIND_USAGE_PARA structure pointer [Security], _CTL_FIND_USAGE_PARA, _crypto2_ctl_find_usage_para, security.ctl_find_usage_para, wincrypt/CTL_FIND_USAGE_PARA, wincrypt/PCTL_FIND_USAGE_PARA"
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
req.typenames: CTL_FIND_USAGE_PARA, *PCTL_FIND_USAGE_PARA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CTL_FIND_USAGE_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CTL_FIND_USAGE_PARA structure


## -description


The <b>CTL_FIND_USAGE_PARA</b> structure is a member of the 
<a href="https://msdn.microsoft.com/b3a63010-9025-4a86-aa48-bfb6e800a07a">CTL_FIND_SUBJECT_PARA</a> structure and it is used by 
<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field SubjectUsage


<a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CTL_USAGE</a> structure that includes a sequence of object identifiers to be matched when finding a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL). 




A found CTL must contain all the usage object identifiers specified by the <b>SubjectUsage</b> member.

If the <b>cUsageIdentifier</b> member of this structure is zero, a CTL with any usage can be a match.


### -field ListIdentifier

Specified to restrict a search to a particular signer CTL list. Normally the <b>ListIdentifier</b> member will be zero, indicating that any <b>ListIdentifier</b> can be matched. If it is not zero, this <b>ListIdentifier</b> and the <b>ListIdentifier</b> in a CTL must match. 




To match only CTLs that have no <b>ListIdentifier</b> the <b>cbData</b> member of <b>ListIdentifier</b> is set to CTL_FIND_NO_LIST_ID_CBDATA.

A CTL uses a <b>ListIdentifier</b> to distinguish among multiple CTLs created by the same issuer with the same <b>SubjectUsage</b>.


### -field pSigner

A pointer to a 
<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure that specifies the CTL signer to be matched. Only the issuer and serial number from the <b>CERT_INFO</b> are used to match a signer. 




Set <b>pSigner</b> to <b>NULL</b> to match any signer. To match CTLs that do not have any signers, set <b>pSigner</b> to CTL_FIND_NO_SIGNER_PTR.

The CertEncodingType of the signer is obtained from the <i>dwMsgAndCertEncodingType</i> parameter of 
<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>.


## -see-also




<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/b3a63010-9025-4a86-aa48-bfb6e800a07a">CTL_FIND_SUBJECT_PARA</a>



<a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CTL_USAGE</a>



<a href="https://msdn.microsoft.com/e5ed3b22-e96f-4e7d-a20e-eebed0a84d3c">CertFindCTLInStore</a>
 

 

