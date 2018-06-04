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

# CertFindSubjectInSortedCTL function


## -description


The <b>CertFindSubjectInSortedCTL</b> function attempts to find the specified subject in a sorted <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL). A subject can be identified either by the certificate's whole context or by any unique identifier of the certificate's subject, such as the SHA1 <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> of the certificate's issuer and serial number.


## -parameters




### -param pSubjectIdentifier [in]

A pointer to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure uniquely identifying the subject. The information in this structure can be a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> or any unique byte sequence.


### -param pCtlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure to be searched.


### -param dwFlags [in]

Reserved for future use and must be <b>NULL</b>.


### -param pvReserved [in]

Reserved for future use and must be <b>NULL</b>.


### -param pEncodedAttributes [out]

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure containing a byte count and a pointer to the subject's encoded attributes.


## -returns



If the function succeeds and the subject identifier exists in the CTL, the return value is <b>TRUE</b>.

If the function fails and does not locate a matching subject identifier, the return value is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/b37cff03-5e9c-4e6c-b46e-d3f02dbf8783">CertEnumSubjectInSortedCTL</a>



<a href="cryptography_functions.htm">Certificate and Certificate Store Maintenance Functions</a>
 

 

