---
UID: NS:appxpackaging.APPX_ENCRYPTED_PACKAGE_SETTINGS2
title: APPX_ENCRYPTED_PACKAGE_SETTINGS2 (appxpackaging.h)
description: Encrypted Windows app package settings.
helpviewer_keywords: ["APPX_ENCRYPTED_PACKAGE_SETTINGS2","APPX_ENCRYPTED_PACKAGE_SETTINGS2 structure [App packaging and management]","PAPPX_ENCRYPTED_PACKAGE_SETTINGS2","PAPPX_ENCRYPTED_PACKAGE_SETTINGS2 structure pointer [App packaging and management]","appxpackaging/APPX_ENCRYPTED_PACKAGE_SETTINGS2","appxpackaging/PAPPX_ENCRYPTED_PACKAGE_SETTINGS2","appxpkg.appx_encrypted_package_settings2"]
old-location: appxpkg\appx_encrypted_package_settings2.htm
tech.root: appxpkg
ms.assetid: 6FAF4B40-0C52-4B9C-8353-1BE4F3D309C4
ms.date: 12/05/2018
ms.keywords: APPX_ENCRYPTED_PACKAGE_SETTINGS2, APPX_ENCRYPTED_PACKAGE_SETTINGS2 structure [App packaging and management], PAPPX_ENCRYPTED_PACKAGE_SETTINGS2, PAPPX_ENCRYPTED_PACKAGE_SETTINGS2 structure pointer [App packaging and management], appxpackaging/APPX_ENCRYPTED_PACKAGE_SETTINGS2, appxpackaging/PAPPX_ENCRYPTED_PACKAGE_SETTINGS2, appxpkg.appx_encrypted_package_settings2
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
req.typenames: APPX_ENCRYPTED_PACKAGE_SETTINGS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPX_ENCRYPTED_PACKAGE_SETTINGS2
 - appxpackaging/APPX_ENCRYPTED_PACKAGE_SETTINGS2
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
 - APPX_ENCRYPTED_PACKAGE_SETTINGS2
---

# APPX_ENCRYPTED_PACKAGE_SETTINGS2 structure


## -description

Encrypted Windows app package settings. This structure expands on <a href="/windows/desktop/api/appxpackaging/ns-appxpackaging-appx_encrypted_package_settings">APPX_ENCRYPTED_PACKAGE_SETTINGS</a>.

## -struct-fields

### -field keyLength

The key length.

### -field encryptionAlgorithm

The encryption algorithm used.

### -field blockMapHashAlgorithm

The Uri of the block map hash algorithm.

### -field options

Additional options for encrypted packages. Options come from the <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_encrypted_package_options">APPX_ENCRYPTED_PACKAGE_OPTIONS</a> enum.