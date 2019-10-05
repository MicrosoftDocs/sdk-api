---
UID: NS:appmodel.PACKAGE_ID
title: PACKAGE_ID (appmodel.h)
author: windows-sdk-content
description: Represents package identification information, such as name, version, and publisher.
old-location: appxpkg\package_id.htm
tech.root: appxpkg
ms.assetid: 4B15281A-2227-47B7-A750-0A01DB8543FC
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PACKAGE_ID, PACKAGE_ID structure [App packaging and management], appmodel/PACKAGE_IDW, appxpkg.package_id
ms.topic: struct
f1_keywords: 
 - "appmodel/PACKAGE_ID"
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
 - PACKAGE_ID
targetos: Windows
req.typenames: PACKAGE_ID
req.redist: 
ms.custom: 19H1
---

# PACKAGE_ID structure


## -description


Represents package identification information, such as name, version, and publisher.


## -struct-fields




### -field reserved

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT32</a></b>

Reserved; do not use.


### -field processorArchitecture

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT32</a></b>

The processor architecture of the package. This member must be one of the values of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_package_architecture">APPX_PACKAGE_ARCHITECTURE</a> enumeration.


### -field version

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/appmodel/ns-appmodel-package_version">PACKAGE_VERSION</a></b>

The version of the package.


### -field name

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

The name of the package.


### -field publisher

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

The publisher of the package. If there is no publisher for the package, this member is <b>NULL</b>.


### -field resourceId

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

The resource identifier (ID) of the package. If there is no resource ID for the package, this member is <b>NULL</b>.


### -field publisherId

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">PWSTR</a></b>

The publisher identifier (ID) of the package. If there is no publisher ID for the package, this member is <b>NULL</b>.


## -remarks



For info about string size limits, see <a href="https://docs.microsoft.com/windows/desktop/appxpkg/identity-constants">Identity constants</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackageid">GetCurrentPackageId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getpackageid">GetPackageId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getpackagepath">GetPackagePath</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/ns-appmodel-package_info">PACKAGE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-packagefamilynamefromid">PackageFamilyNameFromId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-packagefullnamefromid">PackageFullNameFromId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-packageidfromfullname">PackageIdFromFullName</a>
 

 

