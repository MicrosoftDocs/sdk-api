---
UID: NS:appxpackaging.APPX_PACKAGE_SETTINGS
title: APPX_PACKAGE_SETTINGS
author: windows-sdk-content
description: Represents package settings used to create a package.
old-location: appxpkg\appx_package_settings.htm
tech.root: appxpkg
ms.assetid: 85874BCD-44EF-4442-96B8-F22AC4247DB4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: APPX_PACKAGE_SETTINGS, APPX_PACKAGE_SETTINGS structure [App packaging and management], appxpackaging/APPX_PACKAGE_SETTINGS, appxpkg.appx_package_settings
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AppxPackaging.h
api_name:
 - APPX_PACKAGE_SETTINGS
product: Windows
targetos: Windows
req.typenames: APPX_PACKAGE_SETTINGS
req.redist: 
---

# APPX_PACKAGE_SETTINGS structure


## -description


Represents package settings used to create a package.


## -struct-fields




### -field forceZip32

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the package is created as Zip32; <b>FALSE</b> if the package is created as Zip64. The default is Zip64.


### -field hashMethod

Type: <b><b>IUri</b>*</b>

The hash algorithm URI to use for the block map of the package.


## -remarks



Set <b>forceZip32</b> to <b>TRUE</b> to maintain compatibility with older ZIP tools.

The possible values for <b>hashMethod</b> are: <ul>
<li>http://www.w3.org/2001/04/xmlenc#sha256</li>
<li>http://www.w3.org/2001/04/xmldsig-more#sha384</li>
<li>http://www.w3.org/2001/04/xmlenc#sha512</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/10E9250E-7A64-4FB0-ACB9-10CB144A0FBE">IAppxFactory::CreatePackageWriter</a>
 

 

