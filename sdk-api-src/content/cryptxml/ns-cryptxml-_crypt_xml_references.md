---
UID: NS:cryptxml._CRYPT_XML_REFERENCES
title: "_CRYPT_XML_REFERENCES"
author: windows-sdk-content
description: Defines an array of CRYPT_XML_REFERENCE structures.
old-location: security\crypt_xml_references.htm
old-project: SecCrypto
ms.assetid: 25414b2d-3283-4e2f-a23c-ccebff1409e2
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: "*PCRYPT_XML_REFERENCES, CRYPT_XML_REFERENCES, CRYPT_XML_REFERENCES structure [Security], PCRYPT_XML_REFERENCES, PCRYPT_XML_REFERENCES structure pointer [Security], _CRYPT_XML_REFERENCES, cryptxml/CRYPT_XML_REFERENCES, cryptxml/PCRYPT_XML_REFERENCES, security.crypt_xml_references"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: cryptxml.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CRYPT_XML_REFERENCES, *PCRYPT_XML_REFERENCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cryptxml.h
api_name:
 - CRYPT_XML_REFERENCES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPT_XML_REFERENCES structure


## -description


The <b>CRYPT_XML_REFERENCES</b> structure defines an array of <a href="https://msdn.microsoft.com/en-us/library/Dd433862(v=VS.85).aspx">CRYPT_XML_REFERENCE</a> structures.


## -struct-fields




### -field cReference

The number of elements in the array pointed to by the <b>rgpReference</b> member.


### -field rgpReference

A pointer to an array of  <a href="https://msdn.microsoft.com/en-us/library/Dd433862(v=VS.85).aspx">PCRYPT_XML_REFERENCE</a> structures.

