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

# _BCRYPT_ALGORITHM_IDENTIFIER structure


## -description


The <b>BCRYPT_ALGORITHM_IDENTIFIER</b> structure is used with the <a href="https://msdn.microsoft.com/7fa227c0-2b80-49ab-8a19-72f8444d5507">BCryptEnumAlgorithms</a> function to contain a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic algorithm</a> identifier.


## -struct-fields




### -field pszName

A pointer to a null-terminated Unicode string that contains the string identifier of the algorithm. The <a href="https://msdn.microsoft.com/a05ae7e6-d882-4287-9990-23e4cd340b05">CNG Algorithm Identifiers</a> topic contains the predefined algorithm identifiers.


### -field dwClass

Specifies the class of the algorithm. This can be one of the <a href="https://msdn.microsoft.com/509c89ff-0c73-4e57-9c39-400522f2086e">CNG Interface Identifiers</a>.


### -field dwFlags

A set of flags that specify other information about the algorithm. There are currently no flags defined for this member.


## -see-also




<a href="https://msdn.microsoft.com/7fa227c0-2b80-49ab-8a19-72f8444d5507">BCryptEnumAlgorithms</a>
 

 

