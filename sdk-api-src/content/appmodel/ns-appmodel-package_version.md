---
UID: NS:appmodel.PACKAGE_VERSION
title: PACKAGE_VERSION (appmodel.h)
description: Represents the package version information.
helpviewer_keywords: ["PACKAGE_VERSION","PACKAGE_VERSION structure [App packaging and management]","appmodel/PACKAGE_VERSION","appxpkg.package_version"]
old-location: appxpkg\package_version.htm
tech.root: appxpkg
ms.assetid: 8543DF84-A908-4DF5-AEE6-169FECB2AA97
ms.date: 12/05/2018
ms.keywords: PACKAGE_VERSION, PACKAGE_VERSION structure [App packaging and management], appmodel/PACKAGE_VERSION, appxpkg.package_version
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: PACKAGE_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PACKAGE_VERSION
 - appmodel/PACKAGE_VERSION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppModel.h
api_name:
 - PACKAGE_VERSION
---

# PACKAGE_VERSION structure


## -description

Represents the package version information.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Version

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT64</a></b>

The full version number of the package represented as a single integral value.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Revision

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">USHORT</a></b>

The revision version number of the package.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Build

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">USHORT</a></b>

The build version number of the package.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Minor

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">USHORT</a></b>

The minor version number of the package.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Major

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">USHORT</a></b>

The major version number of the package.

## -see-also

<a href="/windows/desktop/api/appmodel/ns-appmodel-package_id">PACKAGE_ID</a>