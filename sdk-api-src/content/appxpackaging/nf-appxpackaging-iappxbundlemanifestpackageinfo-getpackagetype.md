---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetPackageType
title: IAppxBundleManifestPackageInfo::GetPackageType
author: windows-sdk-content
description: Retrieves the type of package that is represented by the package info.
old-location: appxpkg\iappxbundlemanifestpackageinfo_getpackagetype.htm
old-project: appxpkg
ms.assetid: 965E48E3-7C60-4299-85F4-07CB879E7B39
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetPackageType, GetPackageType method [App packaging and management], GetPackageType method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetPackageType method, IAppxBundleManifestPackageInfo.GetPackageType, IAppxBundleManifestPackageInfo::GetPackageType, appxpackaging/IAppxBundleManifestPackageInfo::GetPackageType, appxpkg.iappxbundlemanifestpackageinfo_getpackagetype
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxBundleManifestPackageInfo.GetPackageType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestPackageInfo::GetPackageType


## -description


Retrieves the type of package that is represented by the package info.


## -parameters




### -param packageType [out, retval]

Type: <b><a href="https://msdn.microsoft.com/90A53E6D-D6DD-4E26-A343-9E6888675348">APPX_BUNDLE_PAYLOAD_PACKAGE_TYPE</a>*</b>

The type of package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B9272875-E02A-4443-82B3-C64104E8291C">IAppxBundleManifestPackageInfo</a>
 

 

