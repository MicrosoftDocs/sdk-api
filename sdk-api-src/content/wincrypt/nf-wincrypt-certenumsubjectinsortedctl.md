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

# CertEnumSubjectInSortedCTL function


## -description


The <b>CertEnumSubjectInSortedCTL</b> function retrieves the first or next TrustedSubject in a sorted <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL). A sorted CTL is a CTL created with the CERT_CREATE_CONTEXT_SORTED_FLAG set. Used in a loop, this function can retrieve in sequence all TrustedSubjects in a sorted CTL.


## -parameters




### -param pCtlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure to be searched.


### -param ppvNextSubject [in, out]

A pointer to the address of the last TrustedSubject found. To start the enumeration, <i>ppvNextSubject</i> must point to a pointer  set to <b>NULL</b>. Upon return, the pointer addressed by <i>ppvNextSubject</i> is updated to point to the next TrustedSubject in the encoded sequence.


### -param pSubjectIdentifier [out]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure, uniquely identifying a TrustedSubject. The information in this structure can be a hash or any unique byte sequence.


### -param pEncodedAttributes [out]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure containing a byte count and a pointer to the TrustedSubject's encoded attributes.


## -returns



If the function succeeds, the return value is <b>TRUE</b>, with <i>ppvNextSubject</i> updated to point to the next TrustedSubject in the encoded sequence.

If the function fails, the return value is <b>FALSE</b>. The return value is <b>FALSE</b> if there are no more subjects or there is an argument that is not valid.




## -remarks



The <b>pbData</b> members of <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structures point directly to the encoded bytes. The <b>CRYPT_DER_BLOB</b> structures, themselves, must be allocated and freed by the application, but the memory addressed by the <b>pbData</b> members of these structures is not allocated by the application and must not be freed by the application.

If the CTL is not sorted with the CERT_CREATE_CONTEXT_SORTED_FLAG flag set, an error results.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/027e89e6-3de0-440d-be70-2281778f9a1e">CertFindSubjectInSortedCTL</a>



<a href="cryptography_functions.htm">Certificate and Certificate Store Maintenance Functions</a>
 

 

