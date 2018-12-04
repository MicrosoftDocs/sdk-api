---
UID: NF:appxpackaging.IAppxBundleWriter3.AddPackageReference
title: IAppxBundleWriter3::AddPackageReference
author: windows-sdk-content
description: Adds a reference to an optional app package or a payload file within an app bundle.
old-location: appxpkg\iappxbundlewriter3_addpackagereference.htm
tech.root: appxpkg
ms.assetid: 99969971-9153-47C9-AF9C-7BF1D56EC54D
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AddPackageReference, AddPackageReference method [App packaging and management], AddPackageReference method [App packaging and management],IAppxBundleWriter3 interface, IAppxBundleWriter3 interface [App packaging and management],AddPackageReference method, IAppxBundleWriter3.AddPackageReference, IAppxBundleWriter3::AddPackageReference, appxpackaging/IAppxBundleWriter3::AddPackageReference, appxpkg.iappxbundlewriter3_addpackagereference
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
 - IAppxBundleWriter3.AddPackageReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleWriter3::AddPackageReference


## -description


Adds a reference to an optional app package or a payload file within an app bundle.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param inputStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of <i>fileName</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



By adding a reference to a payload file or optional app package to an app bundle, the overall size of the bundle is reduced.




## -see-also




<a href="https://msdn.microsoft.com/2596E2DA-D9B6-4BBE-AC05-5CE253CE6DDC">IAppxBundleWriter3</a>
 

 

