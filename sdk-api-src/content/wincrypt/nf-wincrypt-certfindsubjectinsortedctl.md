---
UID: NF:wincrypt.CertFindSubjectInSortedCTL
title: CertFindSubjectInSortedCTL function
author: windows-sdk-content
description: The CertFindSubjectInSortedCTL function attempts to find the specified subject in a sorted certificate trust list (CTL).
old-location: security\certfindsubjectinsortedctl.htm
old-project: seccrypto
ms.assetid: 027e89e6-3de0-440d-be70-2281778f9a1e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CertFindSubjectInSortedCTL, CertFindSubjectInSortedCTL function [Security], _crypto2_certfindsubjectinsortedctl, security.certfindsubjectinsortedctl, wincrypt/CertFindSubjectInSortedCTL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFindSubjectInSortedCTL
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
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



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate and Certificate Store Maintenance Functions</a>
 

 

