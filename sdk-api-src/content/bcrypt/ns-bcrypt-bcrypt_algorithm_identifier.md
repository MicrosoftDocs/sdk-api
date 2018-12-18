---
UID: NS:bcrypt._BCRYPT_ALGORITHM_IDENTIFIER
title: BCRYPT_ALGORITHM_IDENTIFIER
author: windows-sdk-content
description: Is used with the BCryptEnumAlgorithms function to contain a cryptographic algorithm identifier.
old-location: security\bcrypt_algorithm_identifier_struct.htm
tech.root: seccng
ms.assetid: a49a21c9-5668-4709-b52a-f6cacd944845
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BCRYPT_ALGORITHM_IDENTIFIER, BCRYPT_ALGORITHM_IDENTIFIER structure [Security], bcrypt/BCRYPT_ALGORITHM_IDENTIFIER, security.bcrypt_algorithm_identifier_struct
ms.topic: struct
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Bcrypt.h
api_name:
 - BCRYPT_ALGORITHM_IDENTIFIER
product: Windows
targetos: Windows
req.typenames: BCRYPT_ALGORITHM_IDENTIFIER
req.redist: 
---

# BCRYPT_ALGORITHM_IDENTIFIER structure


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
 

 

