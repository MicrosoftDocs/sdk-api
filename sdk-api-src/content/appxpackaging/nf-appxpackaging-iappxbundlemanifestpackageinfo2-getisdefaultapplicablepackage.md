---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage
title: IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage
author: windows-sdk-content
description: Determines whether the app package is a default applicable package.
old-location: appxpkg\iappxbundlemanifestpackageinfo2_getisdefaultapplicablepackage.htm
old-project: appxpkg
ms.assetid: 0C1181F5-0BD9-4F8E-A4E3-75A562ADF56A
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: GetIsDefaultApplicablePackage, GetIsDefaultApplicablePackage method [App packaging and management], GetIsDefaultApplicablePackage method [App packaging and management],IAppxBundleManifestPackageInfo2 interface, IAppxBundleManifestPackageInfo2 interface [App packaging and management],GetIsDefaultApplicablePackage method, IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage, IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage, appxpackaging/IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage, appxpkg.iappxbundlemanifestpackageinfo2_getisdefaultapplicablepackage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleManifestPackageInfo2.GetIsDefaultApplicablePackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfo2::GetIsDefaultApplicablePackage


## -description


Determines whether the app package is a default applicable package.


## -parameters




### -param isDefaultApplicablePackage [out, retval]

True if the package is a default applicable package, False otherwise.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A default applicable package is a package that contains the default MRT-qualified resources. For example, a default applicable package could be English language resources that should be installed by default if no other appropriate alternative language is  available.

For more information on app resources, see <a href="https://docs.microsoft.com/windows/uwp/app-resources/">App resources and the Resource Management System</a>.




## -see-also




<a href="https://msdn.microsoft.com/036CD1E1-F4D7-46B9-A287-2728BA45348A">IAppxBundleManifestPackageInfo2</a>
 

 

