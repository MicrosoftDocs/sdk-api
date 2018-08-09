---
UID: NS:appxpackaging.APPX_ENCRYPTED_PACKAGE_SETTINGS2
title: APPX_ENCRYPTED_PACKAGE_SETTINGS2
author: windows-sdk-content
description: Encrypted Windows app package settings.
old-location: appxpkg\appx_encrypted_package_settings2.htm
old-project: appxpkg
ms.assetid: 6FAF4B40-0C52-4B9C-8353-1BE4F3D309C4
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: APPX_ENCRYPTED_PACKAGE_SETTINGS2, APPX_ENCRYPTED_PACKAGE_SETTINGS2 structure [App packaging and management], PAPPX_ENCRYPTED_PACKAGE_SETTINGS2, PAPPX_ENCRYPTED_PACKAGE_SETTINGS2 structure pointer [App packaging and management], appxpackaging/APPX_ENCRYPTED_PACKAGE_SETTINGS2, appxpackaging/PAPPX_ENCRYPTED_PACKAGE_SETTINGS2, appxpkg.appx_encrypted_package_settings2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: APPX_ENCRYPTED_PACKAGE_SETTINGS2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppxPackaging.h
api_name:
 - APPX_ENCRYPTED_PACKAGE_SETTINGS2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

