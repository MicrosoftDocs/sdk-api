---
UID: NE:appxpackaging.APPX_FOOTPRINT_FILE_TYPE
title: APPX_FOOTPRINT_FILE_TYPE (appxpackaging.h)
description: Specifies the type of footprint file in a package.
helpviewer_keywords: ["APPX_FOOTPRINT_FILE_TYPE","APPX_FOOTPRINT_FILE_TYPE enumeration [App packaging and management]","APPX_FOOTPRINT_FILE_TYPE_BLOCKMAP","APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY","APPX_FOOTPRINT_FILE_TYPE_CONTENTGROUPMAP","APPX_FOOTPRINT_FILE_TYPE_MANIFEST","APPX_FOOTPRINT_FILE_TYPE_SIGNATURE","appxpackaging/APPX_FOOTPRINT_FILE_TYPE","appxpackaging/APPX_FOOTPRINT_FILE_TYPE_BLOCKMAP","appxpackaging/APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY","appxpackaging/APPX_FOOTPRINT_FILE_TYPE_CONTENTGROUPMAP","appxpackaging/APPX_FOOTPRINT_FILE_TYPE_MANIFEST","appxpackaging/APPX_FOOTPRINT_FILE_TYPE_SIGNATURE","appxpkg.appx_footprint_file_type"]
old-location: appxpkg\appx_footprint_file_type.htm
tech.root: appxpkg
ms.assetid: AF158108-06E5-45D5-BD64-DA3CEFFB88F0
ms.date: 12/05/2018
ms.keywords: APPX_FOOTPRINT_FILE_TYPE, APPX_FOOTPRINT_FILE_TYPE enumeration [App packaging and management], APPX_FOOTPRINT_FILE_TYPE_BLOCKMAP, APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY, APPX_FOOTPRINT_FILE_TYPE_CONTENTGROUPMAP, APPX_FOOTPRINT_FILE_TYPE_MANIFEST, APPX_FOOTPRINT_FILE_TYPE_SIGNATURE, appxpackaging/APPX_FOOTPRINT_FILE_TYPE, appxpackaging/APPX_FOOTPRINT_FILE_TYPE_BLOCKMAP, appxpackaging/APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY, appxpackaging/APPX_FOOTPRINT_FILE_TYPE_CONTENTGROUPMAP, appxpackaging/APPX_FOOTPRINT_FILE_TYPE_MANIFEST, appxpackaging/APPX_FOOTPRINT_FILE_TYPE_SIGNATURE, appxpkg.appx_footprint_file_type
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: APPX_FOOTPRINT_FILE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPX_FOOTPRINT_FILE_TYPE
 - appxpackaging/APPX_FOOTPRINT_FILE_TYPE
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
 - APPX_FOOTPRINT_FILE_TYPE
---

# APPX_FOOTPRINT_FILE_TYPE enumeration


## -description

Specifies the type of footprint file in a package.

## -enum-fields

### -field APPX_FOOTPRINT_FILE_TYPE_MANIFEST

The package manifest.

### -field APPX_FOOTPRINT_FILE_TYPE_BLOCKMAP

The package block map.

### -field APPX_FOOTPRINT_FILE_TYPE_SIGNATURE

The package signature.

### -field APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY

The code signing catalog file used for code integrity checks.

### -field APPX_FOOTPRINT_FILE_TYPE_CONTENTGROUPMAP

The content group map used for streaming install.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile">IAppxPackageReader::GetFootprintFile</a>