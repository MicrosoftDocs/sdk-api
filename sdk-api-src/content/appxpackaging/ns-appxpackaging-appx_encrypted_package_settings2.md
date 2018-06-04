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

# APPX_ENCRYPTED_PACKAGE_SETTINGS2 structure


## -description


Encrypted Windows app package settings. This structure expands on <a href="https://msdn.microsoft.com/B5502C1D-2C92-4AE6-BC01-50A853D25CE5">APPX_ENCRYPTED_PACKAGE_SETTINGS</a>.


## -struct-fields




### -field keyLength

The key length.


### -field encryptionAlgorithm

The encryption algorithm used.


### -field blockMapHashAlgorithm

The Uri of the block map hash algorithm.


### -field options

Additional options for encrypted packages. Options come from the <a href="https://msdn.microsoft.com/BEF0AA21-AC0F-4DA5-BA5C-404E54B67953">APPX_ENCRYPTED_PACKAGE_OPTIONS</a> enum.

