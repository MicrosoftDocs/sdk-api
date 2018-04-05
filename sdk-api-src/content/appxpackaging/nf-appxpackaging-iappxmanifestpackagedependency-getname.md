---
UID: NF:appxpackaging.IAppxManifestPackageDependency.GetName
title: IAppxManifestPackageDependency::GetName method
author: windows-driver-content
description: Gets the name of the package on which the current package has a dependency.
old-location: appxpkg\iappxmanifestpackagedependency_getname.htm
old-project: appxpkg
ms.assetid: 0B1888D7-04E6-4684-8131-8295EF2C598B
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: GetName method [App packaging and management], GetName method [App packaging and management], IAppxManifestPackageDependency interface, GetName,IAppxManifestPackageDependency.GetName, IAppxManifestPackageDependency, IAppxManifestPackageDependency interface [App packaging and management], GetName method, IAppxManifestPackageDependency::GetName, appxpackaging/IAppxManifestPackageDependency::GetName, appxpkg.iappxmanifestpackagedependency_getname
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
-	IAppxManifestPackageDependency.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageDependency::GetName method


## -description


Gets the name of the package on which the current package has a dependency.


## -parameters




### -param name [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The name of the package.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



The caller must free the memory allocated for <i>name</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA">IAppxManifestPackageDependency</a>
 

 

