---
UID: NF:appxpackaging.IAppxManifestPackageId.GetPackageFamilyName
title: IAppxManifestPackageId::GetPackageFamilyName method
author: windows-driver-content
description: Gets the package family name.
old-location: appxpkg\iappxmanifestpackageid_getpackagefamilyname.htm
old-project: appxpkg
ms.assetid: A4505020-61CB-4893-AB3B-6EF0E55FD225
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetPackageFamilyName method [App packaging and management], GetPackageFamilyName method [App packaging and management], IAppxManifestPackageId interface, GetPackageFamilyName,IAppxManifestPackageId.GetPackageFamilyName, IAppxManifestPackageId, IAppxManifestPackageId interface [App packaging and management], GetPackageFamilyName method, IAppxManifestPackageId::GetPackageFamilyName, appxpackaging/IAppxManifestPackageId::GetPackageFamilyName, appxpkg.iappxmanifestpackageid_getpackagefamilyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: APPX_PACKAGE_ARCHITECTURE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestPackageId.GetPackageFamilyName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageId::GetPackageFamilyName method


## -description


Gets the package family name.


## -parameters




### -param packageFamilyName [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The package family name.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



The package family name is a case-insensitive string, which can be used to uniquely identify a family of packages with the same name and publisher. 

This string is a serialized form of the package ID, and it is suitable for naming objects such as files and directories. Because the package family name does not contain information about package version, architecture, or resources, it is useful when you need a version-independent reference to a package.

The caller must free the memory for <i>packageFamilyName</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>
 

 

