---
UID: NE:appxpackaging.APPX_BUNDLE_FOOTPRINT_FILE_TYPE
title: APPX_BUNDLE_FOOTPRINT_FILE_TYPE (appxpackaging.h)
description: Specifies the type of footprint file in a bundle.
helpviewer_keywords: ["APPX_BUNDLE_FOOTPRINT_FILE_TYPE","APPX_BUNDLE_FOOTPRINT_FILE_TYPE enumeration [App packaging and management]","APPX_BUNDLE_FOOTPRINT_FILE_TYPE_BLOCKMAP","APPX_BUNDLE_FOOTPRINT_FILE_TYPE_FIRST","APPX_BUNDLE_FOOTPRINT_FILE_TYPE_LAST","APPX_BUNDLE_FOOTPRINT_FILE_TYPE_MANIFEST","APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE","appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE","appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_BLOCKMAP","appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_FIRST","appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_LAST","appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_MANIFEST","appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE","appxpkg.appx_bundle_footprint_file_type"]
old-location: appxpkg\appx_bundle_footprint_file_type.htm
tech.root: appxpkg
ms.assetid: 1BC2B15B-9DF3-48D8-B7BE-BEC1E5D7E6E3
ms.date: 12/05/2018
ms.keywords: APPX_BUNDLE_FOOTPRINT_FILE_TYPE, APPX_BUNDLE_FOOTPRINT_FILE_TYPE enumeration [App packaging and management], APPX_BUNDLE_FOOTPRINT_FILE_TYPE_BLOCKMAP, APPX_BUNDLE_FOOTPRINT_FILE_TYPE_FIRST, APPX_BUNDLE_FOOTPRINT_FILE_TYPE_LAST, APPX_BUNDLE_FOOTPRINT_FILE_TYPE_MANIFEST, APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE, appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE, appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_BLOCKMAP, appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_FIRST, appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_LAST, appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_MANIFEST, appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE, appxpkg.appx_bundle_footprint_file_type
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: APPX_BUNDLE_FOOTPRINT_FILE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPX_BUNDLE_FOOTPRINT_FILE_TYPE
 - appxpackaging/APPX_BUNDLE_FOOTPRINT_FILE_TYPE
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
 - APPX_BUNDLE_FOOTPRINT_FILE_TYPE
---

# APPX_BUNDLE_FOOTPRINT_FILE_TYPE enumeration


## -description

Specifies the type of footprint file in a bundle.

## -enum-fields

### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_FIRST

The bundle's first footprint file, which is the bundle manifest.

### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_MANIFEST

The bundle manifest.

### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_BLOCKMAP

The bundle block map.

### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE

The bundle signature.

### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_LAST

The bundle's last footprint file, which is the bundle signature.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getfootprintfile">IAppxBundleReader::GetFootprintFile</a>