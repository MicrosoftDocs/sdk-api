---
UID: NS:appxpackaging.APPX_PACKAGE_SETTINGS
title: APPX_PACKAGE_SETTINGS (appxpackaging.h)
description: Represents package settings used to create a package.
helpviewer_keywords: ["APPX_PACKAGE_SETTINGS","APPX_PACKAGE_SETTINGS structure [App packaging and management]","appxpackaging/APPX_PACKAGE_SETTINGS","appxpkg.appx_package_settings"]
old-location: appxpkg\appx_package_settings.htm
tech.root: appxpkg
ms.assetid: 85874BCD-44EF-4442-96B8-F22AC4247DB4
ms.date: 12/05/2018
ms.keywords: APPX_PACKAGE_SETTINGS, APPX_PACKAGE_SETTINGS structure [App packaging and management], appxpackaging/APPX_PACKAGE_SETTINGS, appxpkg.appx_package_settings
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
req.typenames: APPX_PACKAGE_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - APPX_PACKAGE_SETTINGS
 - appxpackaging/APPX_PACKAGE_SETTINGS
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
 - APPX_PACKAGE_SETTINGS
---

# APPX_PACKAGE_SETTINGS structure


## -description

Represents package settings used to create a package.

## -struct-fields

### -field forceZip32

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the package is created as Zip32; <b>FALSE</b> if the package is created as Zip64. The default is Zip64.

### -field hashMethod

Type: <b>IUri*</b>

The hash algorithm URI to use for the block map of the package.

## -remarks

Set <b>forceZip32</b> to <b>TRUE</b> to maintain compatibility with older ZIP tools.

The possible values for <b>hashMethod</b> are: <ul>
<li>http://www.w3.org/2001/04/xmlenc#sha256</li>
<li>http://www.w3.org/2001/04/xmldsig-more#sha384</li>
<li>http://www.w3.org/2001/04/xmlenc#sha512</li>
</ul>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createpackagewriter">IAppxFactory::CreatePackageWriter</a>