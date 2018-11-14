---
UID: NF:appxpackaging.IAppxManifestPackageDependency2.GetMaxMajorVersionTested
title: IAppxManifestPackageDependency2::GetMaxMajorVersionTested
author: windows-sdk-content
description: Returns the maximum major version number of the package that is tested to be compatible with the current package.
old-location: appxpkg\iappxmanifestpackagedependency2_getmaxmajorversiontested.htm
tech.root: appxpkg
ms.assetid: BB83C97E-9E89-440C-8A14-88062F1394CF
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetMaxMajorVersionTested, GetMaxMajorVersionTested method [App packaging and management], GetMaxMajorVersionTested method [App packaging and management],IAppxManifestPackageDependency2 interface, IAppxManifestPackageDependency2 interface [App packaging and management],GetMaxMajorVersionTested method, IAppxManifestPackageDependency2.GetMaxMajorVersionTested, IAppxManifestPackageDependency2::GetMaxMajorVersionTested, appxpackaging/IAppxManifestPackageDependency2::GetMaxMajorVersionTested, appxpkg.iappxmanifestpackagedependency2_getmaxmajorversiontested
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxManifestPackageDependency2.GetMaxMajorVersionTested
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- appxpackaging.h
: 
- IAppxManifestPackageDependency2.GetMaxMajorVersionTested
: 
---

# IAppxManifestPackageDependency2::GetMaxMajorVersionTested


## -description


Returns the maximum major version number of  the package that is tested to be compatible
with the current package.


## -parameters




### -param maxMajorVersionTested [out]

The maximum major version number of the dependency package that has been tested to be compatible
with the current package.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If the
<b>MaxMajorVersionTested</b> attribute is not specified for the current dependency package, this method returns the highest 16 bits of the <b>MinVersion</b> field. For more information, see the <a href="https://msdn.microsoft.com/301053BA-A2DB-405C-9E2E-3817B2B5D7FD">GetMinVersion</a> method.




## -see-also




<a href="https://msdn.microsoft.com/301053BA-A2DB-405C-9E2E-3817B2B5D7FD">GetMinVersion</a>



<a href="https://msdn.microsoft.com/9363C5BB-BDEF-4671-9545-5B8C0EF14FBE">IAppxManifestPackageDependency2</a>
 

 

