---
UID: NF:appxpackaging.IAppxManifestPackageId.GetResourceId
title: IAppxManifestPackageId::GetResourceId
author: windows-sdk-content
description: Gets the package resource identifier as defined in the manifest.
old-location: appxpkg\iappxmanifestpackageid_getresourceid.htm
old-project: appxpkg
ms.assetid: D17BD71A-6418-4229-8829-2C8EB9393285
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetResourceId, GetResourceId method [App packaging and management], GetResourceId method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetResourceId method, IAppxManifestPackageId.GetResourceId, IAppxManifestPackageId::GetResourceId, appxpackaging/IAppxManifestPackageId::GetResourceId, appxpkg.iappxmanifestpackageid_getresourceid
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
-	IAppxManifestPackageId.GetResourceId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxManifestPackageId::GetResourceId


## -description


Gets the package resource identifier as defined in the manifest.


## -parameters




### -param resourceId [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The resource identifier of the package.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



The resource identifier is specified using the <b>ResourceId</b> attribute of the <a href="https://msdn.microsoft.com/45524773-3b61-44ac-a417-cfaac92af0a0">Identity</a> element in the package manifest.

If no resource identifier is defined in the manifest, this method returns a null string.

The caller must free the memory allocated for <i>resourceId</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>
 

 

