---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetResources
title: IAppxBundleManifestPackageInfo::GetResources
author: windows-sdk-content
description: Retrieves an enumerator that iterates through all the &lt;Resource&gt; elements that are defined in the app package's manifest.
old-location: appxpkg\iappxbundlemanifestpackageinfo_getresources.htm
tech.root: appxpkg
ms.assetid: 07B1028B-4084-44E5-840D-14403E01F628
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetResources, GetResources method [App packaging and management], GetResources method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetResources method, IAppxBundleManifestPackageInfo.GetResources, IAppxBundleManifestPackageInfo::GetResources, appxpackaging/IAppxBundleManifestPackageInfo::GetResources, appxpkg.iappxbundlemanifestpackageinfo_getresources
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleManifestPackageInfo.GetResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleManifestPackageInfo::GetResources


## -description


Retrieves an enumerator that iterates through all the &lt;Resource&gt; elements that are defined in the app package's manifest.


## -parameters




### -param resources [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9F58B665-3C3D-407C-B872-FC915CE97B0E">IAppxManifestQualifiedResourcesEnumerator</a>**</b>

The enumerator that iterates through the resources.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 




## -see-also




<a href="https://msdn.microsoft.com/B9272875-E02A-4443-82B3-C64104E8291C">IAppxBundleManifestPackageInfo</a>
 

 

