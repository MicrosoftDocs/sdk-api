---
UID: NS:mscat.CRYPTCATMEMBER_
title: CRYPTCATMEMBER
author: windows-sdk-content
description: The CRYPTCATMEMBER structure provides information about a catalog member. This structure is used by the CryptCATGetMemberInfo and CryptCATEnumerateAttr functions.
old-location: security\cryptcatmember.htm
tech.root: SecCrypto
ms.assetid: 08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CRYPTCATMEMBER, CRYPTCATMEMBER structure [Security], mscat/CRYPTCATMEMBER, security.cryptcatmember
ms.topic: struct
req.header: mscat.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mscat.h
api_name:
 - CRYPTCATMEMBER
product: Windows
targetos: Windows
req.typenames: CRYPTCATMEMBER
req.redist: 
---

# CRYPTCATMEMBER structure


## -description


<p class="CCE_Message">[The  <b>CRYPTCATMEMBER</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTCATMEMBER</b> structure provides information about a catalog member. This structure is used by the <a href="https://msdn.microsoft.com/ff265232-f57e-4ab0-ba07-05e6d6745ae3">CryptCATGetMemberInfo</a> and <a href="https://msdn.microsoft.com/064e87db-4330-4b8b-9865-ba8b9714f6e4">CryptCATEnumerateAttr</a> functions.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field pwszReferenceTag

A pointer to a null-terminated string that contains the reference tag value.


### -field pwszFileName

A pointer to a null-terminated string that contains the file name.


### -field gSubjectType

<b>GUID</b> that identifies the subject type.


### -field fdwMemberFlags

Value that specifies the member flags.


### -field pIndirectData

A pointer to a <b>SIP_INDIRECT_DATA</b> structure.


### -field dwCertVersion

Value that specifies the certificate version.


### -field dwReserved

Reserved; do not use.


### -field hReserved

Reserved; do not use.


### -field sEncodedIndirectData

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_ATTR_BLOB</a> structure that contains encoded indirect data.


### -field sEncodedMemberInfo

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_ATTR_BLOB</a> structure that contains encoded member information.


## -see-also




<a href="https://msdn.microsoft.com/064e87db-4330-4b8b-9865-ba8b9714f6e4">CryptCATEnumerateAttr</a>



<a href="https://msdn.microsoft.com/ff265232-f57e-4ab0-ba07-05e6d6745ae3">CryptCATGetMemberInfo</a>
 

 

