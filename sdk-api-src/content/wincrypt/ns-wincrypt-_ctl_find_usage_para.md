---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

