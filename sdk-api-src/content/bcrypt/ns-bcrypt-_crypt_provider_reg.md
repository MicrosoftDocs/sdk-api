---
UID: NS:bcrypt._CRYPT_PROVIDER_REG
title: "_CRYPT_PROVIDER_REG"
author: windows-sdk-content
description: Used to contain registration information for a CNG provider.
old-location: security\crypt_provider_reg.htm
tech.root: seccng
ms.assetid: ca0ac386-9435-49f0-95fe-503aa7183517
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PCRYPT_PROVIDER_REG, CRYPT_PROVIDER_REG, CRYPT_PROVIDER_REG structure [Security], PCRYPT_PROVIDER_REG, PCRYPT_PROVIDER_REG structure pointer [Security], _CRYPT_PROVIDER_REG, bcrypt/CRYPT_PROVIDER_REG, bcrypt/PCRYPT_PROVIDER_REG, security.crypt_provider_reg"
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
 - CRYPT_PROVIDER_REG
product: Windows
targetos: Windows
req.typenames: CRYPT_PROVIDER_REG, *PCRYPT_PROVIDER_REG
req.redist: 
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

