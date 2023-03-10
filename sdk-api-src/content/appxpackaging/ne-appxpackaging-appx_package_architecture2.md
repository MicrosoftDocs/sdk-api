---
UID: NE:appxpackaging.APPX_PACKAGE_ARCHITECTURE2
title: APPX_PACKAGE_ARCHITECTURE2 (appxpackaging.h)
description: Specifies the processor architectures supported by a package. (APPX_PACKAGE_ARCHITECTURE2)
helpviewer_keywords: ["APPX_PACKAGE_ARCHITECTURE2","APPX_PACKAGE_ARCHITECTURE2 enumeration [App packaging and management]","APPX_PACKAGE_ARCHITECTURE2_ARM","APPX_PACKAGE_ARCHITECTURE2_ARM64","APPX_PACKAGE_ARCHITECTURE2_NEUTRAL","APPX_PACKAGE_ARCHITECTURE2_UNKNOWN","APPX_PACKAGE_ARCHITECTURE2_X64","APPX_PACKAGE_ARCHITECTURE2_X86","APPX_PACKAGE_ARCHITECTURE2_X86_ON_ARM64","appxpackaging/APPX_PACKAGE_ARCHITECTURE2","appxpackaging/APPX_PACKAGE_ARCHITECTURE2_ARM","appxpackaging/APPX_PACKAGE_ARCHITECTURE2_ARM64","appxpackaging/APPX_PACKAGE_ARCHITECTURE2_NEUTRAL","appxpackaging/APPX_PACKAGE_ARCHITECTURE2_UNKNOWN","appxpackaging/APPX_PACKAGE_ARCHITECTURE2_X64","appxpackaging/APPX_PACKAGE_ARCHITECTURE2_X86","appxpackaging/APPX_PACKAGE_ARCHITECTURE2_X86_ON_ARM64","appxpkg.appx_package_architecture2"]
old-location: appxpkg\appx_package_architecture2.htm
tech.root: appxpkg
ms.assetid: 86E1C7DE-01AD-4682-89C3-20A5A699CBE7
ms.date: 12/05/2018
ms.keywords: APPX_PACKAGE_ARCHITECTURE2, APPX_PACKAGE_ARCHITECTURE2 enumeration [App packaging and management], APPX_PACKAGE_ARCHITECTURE2_ARM, APPX_PACKAGE_ARCHITECTURE2_ARM64, APPX_PACKAGE_ARCHITECTURE2_NEUTRAL, APPX_PACKAGE_ARCHITECTURE2_UNKNOWN, APPX_PACKAGE_ARCHITECTURE2_X64, APPX_PACKAGE_ARCHITECTURE2_X86, APPX_PACKAGE_ARCHITECTURE2_X86_ON_ARM64, appxpackaging/APPX_PACKAGE_ARCHITECTURE2, appxpackaging/APPX_PACKAGE_ARCHITECTURE2_ARM, appxpackaging/APPX_PACKAGE_ARCHITECTURE2_ARM64, appxpackaging/APPX_PACKAGE_ARCHITECTURE2_NEUTRAL, appxpackaging/APPX_PACKAGE_ARCHITECTURE2_UNKNOWN, appxpackaging/APPX_PACKAGE_ARCHITECTURE2_X64, appxpackaging/APPX_PACKAGE_ARCHITECTURE2_X86, appxpackaging/APPX_PACKAGE_ARCHITECTURE2_X86_ON_ARM64, appxpkg.appx_package_architecture2
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPX_PACKAGE_ARCHITECTURE2
 - appxpackaging/APPX_PACKAGE_ARCHITECTURE2
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
 - APPX_PACKAGE_ARCHITECTURE2
---

# APPX_PACKAGE_ARCHITECTURE2 enumeration


## -description

Specifies the processor architectures supported by a package.

## -enum-fields

### -field APPX_PACKAGE_ARCHITECTURE2_X86

The x86, 32-bit processor architecture.

### -field APPX_PACKAGE_ARCHITECTURE2_ARM

The ARM processor architecture.

### -field APPX_PACKAGE_ARCHITECTURE2_X64

The x64, 64-bit processor architecture.

### -field APPX_PACKAGE_ARCHITECTURE2_NEUTRAL

Any  processor architecture.

### -field APPX_PACKAGE_ARCHITECTURE2_ARM64

The 64-bit ARM processor architecture.

### -field APPX_PACKAGE_ARCHITECTURE2_X86_ON_ARM64

A 32-bit app package that runs on a 64-bit ARM processor.

### -field APPX_PACKAGE_ARCHITECTURE2_UNKNOWN

Unknown app package architecture.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackageid-getarchitecture">IAppxManifestPackageId::GetArchitecture</a>
