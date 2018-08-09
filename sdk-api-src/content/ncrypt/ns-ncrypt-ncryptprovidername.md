---
UID: NS:ncrypt.NCryptProviderName
title: NCryptProviderName
author: windows-sdk-content
description: Used to contain the name of a CNG key storage provider.
old-location: security\ncryptprovidername_struct.htm
old-project: seccng
ms.assetid: 21d8bf28-ee3f-4036-b3b0-d9c68cb14fa9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NCryptProviderName, NCryptProviderName structure [Security], ncrypt/NCryptProviderName, security.ncryptprovidername_struct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ncrypt.h
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
req.typenames: NCryptProviderName
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ncrypt.h
api_name:
 - NCryptProviderName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NCryptProviderName structure


## -description


The <b>NCryptProviderName</b> structure is used to contain the name of a CNG key storage provider. This structure is used with the <a href="https://msdn.microsoft.com/24a8ee01-b716-4f36-9df5-b6476b1df4f0">NCryptEnumStorageProviders</a> function to return the names of the registered CNG key storage providers.


## -struct-fields




### -field pszName

A pointer to a null-terminated Unicode string that contains the name of the provider.


### -field pszComment

A pointer to a null-terminated Unicode string that contains optional text for the provider.


## -see-also




<a href="https://msdn.microsoft.com/24a8ee01-b716-4f36-9df5-b6476b1df4f0">NCryptEnumStorageProviders</a>
 

 

