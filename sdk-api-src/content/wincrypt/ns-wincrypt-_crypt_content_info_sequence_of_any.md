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

# _CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY structure


## -description


The <b>CRYPT_CONTENT_INFO_SEQUENCE_OF_ANY</b> structure contains information representing the Netscape certificate sequence of certificates.

A Netscape certificate sequence of certificates can be created by setting the <b>pszObjId</b> member to szOID_NETSCAPE_CERT_SEQUENCE and supplying <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">DER</a>-encoded certificates in <b>rgValue</b>.


## -struct-fields




### -field pszObjId

Object identifier (OID) specifying the type of data contained in the <b>rgValue</b> array.


### -field cValue

Number of elements in the <b>rgValue</b> array.


### -field rgValue

Array of pointers to <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structures. For more information, see 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>.

