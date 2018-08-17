---
UID: NS:bcrypt._BCRYPT_ALGORITHM_IDENTIFIER
title: "_BCRYPT_ALGORITHM_IDENTIFIER"
author: windows-sdk-content
description: Is used with the BCryptEnumAlgorithms function to contain a cryptographic algorithm identifier.
old-location: security\bcrypt_algorithm_identifier_struct.htm
old-project: seccng
ms.assetid: a49a21c9-5668-4709-b52a-f6cacd944845
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BCRYPT_ALGORITHM_IDENTIFIER, BCRYPT_ALGORITHM_IDENTIFIER structure [Security], _BCRYPT_ALGORITHM_IDENTIFIER, bcrypt/BCRYPT_ALGORITHM_IDENTIFIER, security.bcrypt_algorithm_identifier_struct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bcrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BCRYPT_ALGORITHM_IDENTIFIER
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
req.lib: 
req.dll: 
req.irql: 
---

# _BCRYPT_ALGORITHM_IDENTIFIER structure


## -description


The <b>BCRYPT_ALGORITHM_IDENTIFIER</b> structure is used with the <a href="https://msdn.microsoft.com/en-us/library/Aa375422(v=VS.85).aspx">BCryptEnumAlgorithms</a> function to contain a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">cryptographic algorithm</a> identifier.


## -struct-fields




### -field pszName

A pointer to a null-terminated Unicode string that contains the string identifier of the algorithm. The <a href="https://msdn.microsoft.com/en-us/library/Aa375534(v=VS.85).aspx">CNG Algorithm Identifiers</a> topic contains the predefined algorithm identifiers.


### -field dwClass

Specifies the class of the algorithm. This can be one of the <a href="https://msdn.microsoft.com/en-us/library/Aa376201(v=VS.85).aspx">CNG Interface Identifiers</a>.


### -field dwFlags

A set of flags that specify other information about the algorithm. There are currently no flags defined for this member.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375422(v=VS.85).aspx">BCryptEnumAlgorithms</a>
 

 

