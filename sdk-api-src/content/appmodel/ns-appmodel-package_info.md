---
UID: NS:appmodel.PACKAGE_INFO
title: PACKAGE_INFO (appmodel.h)
description: Represents package identification information that includes the package identifier, full name, and install location.helpviewer_keywords: ["PACKAGE_INFO","PACKAGE_INFO structure [App packaging and management]","appmodel/PACKAGE_INFO","appxpkg.package_info"]
old-location: appxpkg\package_info.htm
tech.root: appxpkg
ms.assetid: 0DDE00D1-9C5F-4F2B-8110-A92B1FFA1B64
ms.date: 12/05/2018
ms.keywords: PACKAGE_INFO, PACKAGE_INFO structure [App packaging and management], appmodel/PACKAGE_INFO, appxpkg.package_info
f1_keywords:
- appmodel/PACKAGE_INFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- AppModel.h
api_name:
- PACKAGE_INFO
targetos: Windows
req.typenames: PACKAGE_INFO
req.redist: 
ms.custom: 19H1
---

# PACKAGE_INFO structure


## -description


Represents package identification information that includes the package identifier, full name, and install location.


## -struct-fields




### -field reserved

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT32</a></b>

Reserved; do not use.


### -field flags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT32</a></b>

Properties of the package.


### -field path

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

The location of the package.


### -field packageFullName

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

The package full name.


### -field packageFamilyName

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

The package family name.


### -field packageId

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/appmodel/ns-appmodel-package_id">PACKAGE_ID</a></b>

The package identifier (ID).


## -remarks



For info about string size limits, see <a href="https://docs.microsoft.com/windows/desktop/appxpkg/identity-constants">Identity constants</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackageinfo">GetCurrentPackageInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getpackageinfo">GetPackageInfo</a>
 

 

