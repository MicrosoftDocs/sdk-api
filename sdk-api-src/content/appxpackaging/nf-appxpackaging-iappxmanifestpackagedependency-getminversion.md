---
UID: NF:appxpackaging.IAppxManifestPackageDependency.GetMinVersion
title: IAppxManifestPackageDependency::GetMinVersion
author: windows-sdk-content
description: Gets the minimum version of the package on which the current package has a dependency.
old-location: appxpkg\iappxmanifestpackagedependency_getminversion.htm
old-project: appxpkg
ms.assetid: 301053BA-A2DB-405C-9E2E-3817B2B5D7FD
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetMinVersion, GetMinVersion method [App packaging and management], GetMinVersion method [App packaging and management],IAppxManifestPackageDependency interface, IAppxManifestPackageDependency interface [App packaging and management],GetMinVersion method, IAppxManifestPackageDependency.GetMinVersion, IAppxManifestPackageDependency::GetMinVersion, appxpackaging/IAppxManifestPackageDependency::GetMinVersion, appxpkg.iappxmanifestpackagedependency_getminversion
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxManifestPackageDependency.GetMinVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageDependency::GetMinVersion


## -description


Gets the minimum version of the package on which the current package has a dependency.


## -parameters




### -param minVersion [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a>*</b>

The minimum version of the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the minimum version is not defined for the dependency, this method returns <b>S_OK</b> and <i>minVersion</i> is 0.

The version is specified using the <b>MinVersion</b> attribute of the <a href="https://msdn.microsoft.com/7f0800a1-f1dd-48c2-aba0-3701dd27d383">PackageDependency</a> element in the package manifest. The specification in the manifest is in quad notation:

<i>major</i>.<i>minor</i>.<i>build</i>.<i>revision</i>

This method converts this notation to a <b>UINT64</b> value as follows:

<ul>
<li>The high-order word contains the major version</li>
<li>The next word contains the minor version</li>
<li>The next word contains the build number</li>
<li>The low-order word contains the revision</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA">IAppxManifestPackageDependency</a>
 

 

