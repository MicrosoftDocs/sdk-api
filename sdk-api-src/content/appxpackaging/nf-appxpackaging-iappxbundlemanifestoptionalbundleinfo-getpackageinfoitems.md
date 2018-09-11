---
UID: NF:appxpackaging.IAppxBundleManifestOptionalBundleInfo.GetPackageInfoItems
title: IAppxBundleManifestOptionalBundleInfo::GetPackageInfoItems
author: windows-sdk-content
description: Retrieves optional packages in the bundle.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfo_getpackageinfoitems.htm
tech.root: appxpkg
ms.assetid: 6D5028BF-7C74-4F74-9600-0A423FDC6E85
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: GetPackageInfoItems, GetPackageInfoItems method [App packaging and management], GetPackageInfoItems method [App packaging and management],IAppxBundleManifestOptionalBundleInfo interface, IAppxBundleManifestOptionalBundleInfo interface [App packaging and management],GetPackageInfoItems method, IAppxBundleManifestOptionalBundleInfo.GetPackageInfoItems, IAppxBundleManifestOptionalBundleInfo::GetPackageInfoItems, appxpackaging/IAppxBundleManifestOptionalBundleInfo::GetPackageInfoItems, appxpkg.iappxbundlemanifestoptionalbundleinfo_getpackageinfoitems
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAppxBundleManifestOptionalBundleInfo.GetPackageInfoItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleManifestOptionalBundleInfo::GetPackageInfoItems


## -description


Retrieves optional packages in the bundle.


## -parameters




### -param packageInfoItems [out, retval]

Type: <b>IAppxBundleManifestPackageInfoEnumerator**</b>

 An enumerator over all payload packages in a &lt;OptionalBundle&gt; element of a bundle. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C9DC823D-46D5-4459-A20A-0969D20C6E9E">IAppxBundleManifestOptionalBundleInfo</a>
 

 

