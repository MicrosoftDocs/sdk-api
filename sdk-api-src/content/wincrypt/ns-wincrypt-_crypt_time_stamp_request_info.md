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

# _CRYPT_TIME_STAMP_REQUEST_INFO structure


## -description


The <b>CRYPT_TIME_STAMP_REQUEST_INFO</b> structure is used for time stamping. To add an authenticated attribute when signing an executable file to verify the date and time of the signature, a signed time stamp is requested from a time stamp server. The <b>CRYPT_TIME_STAMP_REQUEST_INFO</b> structure is used to get a time stamp. It contains the signature bits of the material being time stamped in the <b>Content</b> field.


## -struct-fields




### -field pszTimeStampAlgorithm

The <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that specifies the desired format of the time stamp, usually UTC.


### -field pszContentType

The OID of the Content Type of the content, usually DATA.


### -field Content

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> structure that contains the encoded signature bits of the material being time stamped.


### -field cAttribute

The number of elements in the <b>rgAttribute</b> array.
					


### -field rgAttribute

Array of pointers to 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures, each holding an encoded attribute.


## -see-also




<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

