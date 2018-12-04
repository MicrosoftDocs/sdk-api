---
UID: NS:cryptxml._CRYPT_XML_REFERENCE
title: "_CRYPT_XML_REFERENCE"
author: windows-sdk-content
description: Contains information used to populate the Reference element.
old-location: security\crypt_xml_reference.htm
tech.root: seccrypto
ms.assetid: af16af5a-b1e5-4250-bdb1-f3fceb1830b9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PCRYPT_XML_REFERENCE, CRYPT_XML_REFERENCE, CRYPT_XML_REFERENCE structure [Security], PCRYPT_XML_REFERENCE, PCRYPT_XML_REFERENCE structure pointer [Security], _CRYPT_XML_REFERENCE, cryptxml/CRYPT_XML_REFERENCE, cryptxml/PCRYPT_XML_REFERENCE, security.crypt_xml_reference"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Cryptxml.h
api_name:
 - CRYPT_XML_REFERENCE
product: Windows
targetos: Windows
req.typenames: CRYPT_XML_REFERENCE, *PCRYPT_XML_REFERENCE
req.redist: 
---

# _CRYPT_XML_REFERENCE structure


## -description


The <b>CRYPT_XML_REFERENCE</b> structure contains information used to populate the <b>Reference</b> element.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hReference

The handle of the <b>Reference</b> element.


### -field wszId

Optional. A pointer to a null-terminated Unicode string that contains the value of the <b>Id</b> attribute.


### -field wszUri

 A pointer to a null-terminated Unicode string that contains a <b>URI</b> attribute.


### -field wszType

A pointer to a null-terminated Unicode string that contains the value of the <b>Type</b> attribute. 


### -field DigestMethod

A <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the digest method.


### -field DigestValue

A <a href="https://msdn.microsoft.com/1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f">CRYPT_DATA_BLOB</a> structure that specifies the hash value.


### -field cTransform

The number of elements in the array pointed to by the <b>rgTransform</b> member.


### -field rgTransform

An array of <a href="https://msdn.microsoft.com/4821dc8f-11d4-4083-bb17-9d9637d99af5">CRYPT_XML_TRANSFORM_INFO</a> structures  that contain information about the transform applied to the signed data.

