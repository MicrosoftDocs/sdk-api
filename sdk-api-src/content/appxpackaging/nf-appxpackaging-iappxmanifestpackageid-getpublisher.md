---
UID: NF:appxpackaging.IAppxManifestPackageId.GetPublisher
title: IAppxManifestPackageId::GetPublisher (appxpackaging.h)
author: windows-sdk-content
description: Gets the name of the package publisher as defined in the manifest.
old-location: appxpkg\iappxmanifestpackageid_getpublisher.htm
tech.root: appxpkg
ms.assetid: 3C3B937D-5A70-480C-98F1-783D05D1810C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPublisher, GetPublisher method [App packaging and management], GetPublisher method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetPublisher method, IAppxManifestPackageId.GetPublisher, IAppxManifestPackageId::GetPublisher, appxpackaging/IAppxManifestPackageId::GetPublisher, appxpkg.iappxmanifestpackageid_getpublisher
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
 - IAppxManifestPackageId.GetPublisher
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxManifestPackageId::GetPublisher


## -description


Gets the name of the package publisher as defined in the manifest.


## -parameters




### -param publisher [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

The publisher of the package.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -remarks



Publisher name information is specified using the <b>Publisher</b> attribute of the <a href="https://msdn.microsoft.com/45524773-3b61-44ac-a417-cfaac92af0a0">Identity</a> element in the package manifest.

The caller must free the memory allocated for <i>publisher</i> using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/8665AC2B-4D06-4684-99B1-E22533CA04AA">IAppxManifestPackageId</a>
 

 

