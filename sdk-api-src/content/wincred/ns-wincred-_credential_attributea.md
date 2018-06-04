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

# _CREDENTIAL_ATTRIBUTEA structure


## -description


The <b>CREDENTIAL_ATTRIBUTE</b> structure contains an application-defined attribute of the credential. An attribute is a keyword-value pair. It is up to the application to define the meaning of the attribute.


## -struct-fields




### -field Keyword

Name of the application-specific attribute. Names should be of the form &lt;CompanyName&gt;_&lt;Name&gt;. 




This member cannot be longer than CRED_MAX_STRING_LENGTH (256) characters.


### -field Flags

Identifies characteristics of the credential attribute. This member is reserved and should be originally initialized as zero and not otherwise altered to permit future enhancement.


### -field ValueSize

Length of <b>Value</b> in bytes. This member cannot be larger than CRED_MAX_VALUE_SIZE (256).


### -field Value

Data associated with the attribute. By convention, if <b>Value</b> is a text string, then  <b>Value</b> should not include the trailing zero character and should be in UNICODE. 




Credentials are expected to be portable. The application should take care to ensure that the data in value is portable. It is the responsibility of the application to define the byte-endian and alignment of the data in <b>Value</b>.

