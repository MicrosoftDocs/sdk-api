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

# _CERT_BASIC_CONSTRAINTS_INFO structure


## -description


The <b>CERT_BASIC_CONSTRAINTS_INFO</b> structure contains information that indicates whether the certified subject can act as a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA), an end entity, or both. If the subject can act as a CA, a certification path-length constraint can also be specified, as can a set of subtrees that must contain all subject names of subsequent certificates in a certification chain. This extension is used in validating certificates used to sign other certificates.


				The <a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> function creates an instance of this structure when performed on a 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure's <b>Value</b> member with its structure's <b>pszObjId</b> member set to szOID_BASIC_CONSTRAINTS.


## -struct-fields




### -field SubjectType

A
						<a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a> value can contain one of the following:

<ul>
<li>A CERT_CA_SUBJECT_FLAG that, when set, indicates that the certificate's subject can act as a CA.</li>
<li>A CERT_END_ENTITY_SUBJECT_FLAG that, when set, indicates that the certificate's subject can act as an end entity.</li>
<li>Both of the above, combined using a bitwise-<b>OR</b> operation.</li>
</ul>

### -field fPathLenConstraint

A Boolean value that indicates whether the <b>dwPathLenConstraint</b> field sets the maximum length of the certification path.


### -field dwPathLenConstraint

The maximum number of CA certificates that can follow this certificate in a certification validation path. A value of zero indicates that the subject of this certificate can issue certificates only to end entities and not to CAs.


### -field cSubtreesConstraint

The number of elements in the <b>rgSubtreesConstraint</b> array.


### -field rgSubtreesConstraint

An array of 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> structures that establish subtree constraints.


## -see-also




<a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

