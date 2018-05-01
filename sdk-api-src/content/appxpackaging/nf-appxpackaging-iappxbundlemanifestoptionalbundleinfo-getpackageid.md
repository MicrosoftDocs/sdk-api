---
UID: NF:appxpackaging.IAppxBundleManifestOptionalBundleInfo.GetPackageId
title: IAppxBundleManifestOptionalBundleInfo::GetPackageId method
author: windows-driver-content
description: Retrieves an object that represents the identity of the &lt;OptionalBundle&gt;.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfo_getpackageid.htm
old-project: appxpkg
ms.assetid: 57C8FB41-0218-4768-8E84-4ABF63EB94E8
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetPackageId method [App packaging and management], GetPackageId method [App packaging and management], IAppxBundleManifestOptionalBundleInfo interface, GetPackageId,IAppxBundleManifestOptionalBundleInfo.GetPackageId, IAppxBundleManifestOptionalBundleInfo, IAppxBundleManifestOptionalBundleInfo interface [App packaging and management], GetPackageId method, IAppxBundleManifestOptionalBundleInfo::GetPackageId, appxpackaging/IAppxBundleManifestOptionalBundleInfo::GetPackageId, appxpkg.iappxbundlemanifestoptionalbundleinfo_getpackageid
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxBundleManifestOptionalBundleInfo.GetPackageId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestOptionalBundleInfo::GetPackageId method


## -description


Retrieves an object that represents the identity of the &lt;OptionalBundle&gt;.


## -parameters




### -param packageId [out, retval]

The package identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C9DC823D-46D5-4459-A20A-0969D20C6E9E">IAppxBundleManifestOptionalBundleInfo</a>
 

 

