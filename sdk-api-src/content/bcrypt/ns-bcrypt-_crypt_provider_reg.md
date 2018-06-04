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

# _CRYPT_PROVIDER_REG structure


## -description


The <b>CRYPT_PROVIDER_REG</b> structure is used to contain registration information for a CNG provider.


## -struct-fields




### -field cAliases

Contains the number of elements in the <b>rgpszAliases</b> array. If the provider has no aliases, this member will be zero and the <b>rgpszAliases</b> member will be <b>NULL</b>.


### -field rgpszAliases

An array of null-terminated Unicode strings that contains the aliases of the provider. If the provider has no aliases, this member will contain <b>NULL</b> and the <b>cAliases</b> member will contain zero.


### -field pUM

A pointer to a <a href="https://msdn.microsoft.com/d7dc3bd8-3957-4a4c-9959-dc22505e129a">CRYPT_IMAGE_REG</a> structure that contains the registration information for the user mode provider. If this member is <b>NULL</b>, the provider is not registered for user mode.


### -field pKM

A pointer to a <a href="https://msdn.microsoft.com/d7dc3bd8-3957-4a4c-9959-dc22505e129a">CRYPT_IMAGE_REG</a> structure that contains the registration information for the kernel mode provider. If this member is <b>NULL</b>, the provider is not registered for kernel mode.

