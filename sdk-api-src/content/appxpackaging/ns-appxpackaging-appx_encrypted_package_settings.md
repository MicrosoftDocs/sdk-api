---
UID: NS:appxpackaging.APPX_ENCRYPTED_PACKAGE_SETTINGS
title: APPX_ENCRYPTED_PACKAGE_SETTINGS (appxpackaging.h)
description: Settings for encrypted Windows app packages.
helpviewer_keywords: ["APPX_ENCRYPTED_PACKAGE_SETTINGS","APPX_ENCRYPTED_PACKAGE_SETTINGS structure [App packaging and management]","PAPPX_ENCRYPTED_PACKAGE_SETTINGS","PAPPX_ENCRYPTED_PACKAGE_SETTINGS structure pointer [App packaging and management]","appxpackaging/APPX_ENCRYPTED_PACKAGE_SETTINGS","appxpackaging/PAPPX_ENCRYPTED_PACKAGE_SETTINGS","appxpkg.appx_encrypted_package_settings"]
old-location: appxpkg\appx_encrypted_package_settings.htm
tech.root: appxpkg
ms.assetid: B5502C1D-2C92-4AE6-BC01-50A853D25CE5
ms.date: 12/05/2018
ms.keywords: APPX_ENCRYPTED_PACKAGE_SETTINGS, APPX_ENCRYPTED_PACKAGE_SETTINGS structure [App packaging and management], PAPPX_ENCRYPTED_PACKAGE_SETTINGS, PAPPX_ENCRYPTED_PACKAGE_SETTINGS structure pointer [App packaging and management], appxpackaging/APPX_ENCRYPTED_PACKAGE_SETTINGS, appxpackaging/PAPPX_ENCRYPTED_PACKAGE_SETTINGS, appxpkg.appx_encrypted_package_settings
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: APPX_ENCRYPTED_PACKAGE_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPX_ENCRYPTED_PACKAGE_SETTINGS
 - appxpackaging/APPX_ENCRYPTED_PACKAGE_SETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppxPackaging.h
api_name:
 - APPX_ENCRYPTED_PACKAGE_SETTINGS
---

# APPX_ENCRYPTED_PACKAGE_SETTINGS structure


## -description

Settings for encrypted Windows app packages.

## -struct-fields

### -field keyLength

The key length.

### -field encryptionAlgorithm

The encryption algorithm used.

### -field useDiffusion

True is diffusion is used, false otherwise.

### -field blockMapHashAlgorithm

The Uri of the block map hash algorithm.

