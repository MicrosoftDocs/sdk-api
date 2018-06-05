---
UID: NS:bcrypt._BCRYPT_PROVIDER_NAME
title: "_BCRYPT_PROVIDER_NAME"
author: windows-sdk-content
description: Contains the name of a CNG provider.
old-location: security\bcrypt_provider_name_struct.htm
old-project: SecCNG
ms.assetid: 0c57aa3f-1d9a-4bb2-b142-bce9c054e658
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: BCRYPT_PROVIDER_NAME, BCRYPT_PROVIDER_NAME structure [Security], _BCRYPT_PROVIDER_NAME, bcrypt/BCRYPT_PROVIDER_NAME, security.bcrypt_provider_name_struct
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BCRYPT_PROVIDER_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bcrypt.h
api_name:
-	BCRYPT_PROVIDER_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BCRYPT_PROVIDER_NAME structure


## -description


The <b>BCRYPT_PROVIDER_NAME</b> structure contains the name of a CNG provider.


## -struct-fields




### -field pszProviderName

A pointer to a null-terminated Unicode string that contains the name of the provider.


## -see-also




<a href="https://msdn.microsoft.com/0496f241-9530-47fb-89e2-15d7ab6da87a">BCryptEnumProviders</a>
 

 

