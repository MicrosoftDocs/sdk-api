---
UID: NF:appxpackaging.IAppxBundleWriter4.AddPackageReference
title: IAppxBundleWriter4::AddPackageReference (appxpackaging.h)
author: windows-sdk-content
description: Adds a reference to an optional app package or a payload file within an app bundle.
old-location: appxpkg\iappxbundlewriter4_addpackagereference.htm
tech.root: appxpkg
ms.assetid: 16ADE271-C507-4CC4-BB42-E76438B79436
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddPackageReference, AddPackageReference method [App packaging and management], AddPackageReference method [App packaging and management],IAppxBundleWriter4 interface, IAppxBundleWriter4 interface [App packaging and management],AddPackageReference method, IAppxBundleWriter4.AddPackageReference, IAppxBundleWriter4::AddPackageReference, appxpackaging/IAppxBundleWriter4::AddPackageReference, appxpkg.iappxbundlewriter4_addpackagereference
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
 - IAppxBundleWriter4.AddPackageReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleWriter4::AddPackageReference


## -description


Adds a reference to an optional app package or a payload file within an app bundle.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param inputStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of <i>fileName</i>.


### -param isDefaultApplicablePackage [in]

A flag for whether this package is a default applicable package.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0C1181F5-0BD9-4F8E-A4E3-75A562ADF56A">GetIsDefaultApplicablePackage</a>



<a href="https://msdn.microsoft.com/9BB81F38-8451-4D3B-B0B6-31AF3001AB17">IAppxBundleWriter4</a>
 

 

