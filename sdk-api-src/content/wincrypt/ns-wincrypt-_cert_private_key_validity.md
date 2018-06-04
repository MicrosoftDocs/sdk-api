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

# _CERT_PRIVATE_KEY_VALIDITY structure


## -description


The <b>CERT_PRIVATE_KEY_VALIDITY</b> structure indicates a valid time span for the private key corresponding to a certificate's public key. If the <b>NotBefore</b> component is zero or not present, no statement is made as to when the validity period of the private key begins. If the <b>NotAfter</b> component is zero or not present, no end date is set on the validity of the private key.

A <b>CERT_PRIVATE_KEY_VALIDITY</b> structure is a member of the 
<a href="https://msdn.microsoft.com/cedf0321-4f5a-48a9-abfd-d8642bb89576">CERT_KEY_ATTRIBUTES_INFO</a> structure.


## -struct-fields




### -field NotBefore

Date and time before which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized-time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four-digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotBefore</b> time is only precise to seconds.


### -field NotAfter

Date and time after which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotAfter</b> time is only precise to seconds.


## -see-also




<a href="https://msdn.microsoft.com/cedf0321-4f5a-48a9-abfd-d8642bb89576">CERT_KEY_ATTRIBUTES_INFO</a>
 

 

