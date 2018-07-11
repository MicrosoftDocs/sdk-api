---
UID: NF:appxpackaging.IAppxBundleWriter4.AddPayloadPackage
title: IAppxBundleWriter4::AddPayloadPackage
author: windows-sdk-content
description: Adds a new app package to the bundle.
old-location: appxpkg\iappxbundlewriter4_addpayloadpackage.htm
old-project: appxpkg
ms.assetid: 5D313F6C-F2EC-42A4-A4A8-8026E7DBF67B
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: AddPayloadPackage, AddPayloadPackage method [App packaging and management], AddPayloadPackage method [App packaging and management],IAppxBundleWriter4 interface, IAppxBundleWriter4 interface [App packaging and management],AddPayloadPackage method, IAppxBundleWriter4.AddPayloadPackage, IAppxBundleWriter4::AddPayloadPackage, appxpackaging/IAppxBundleWriter4::AddPayloadPackage, appxpkg.iappxbundlewriter4_addpayloadpackage
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxBundleWriter4.AddPayloadPackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleWriter4::AddPayloadPackage


## -description


Adds a new app package to the bundle.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param packageStream




### -param isDefaultApplicablePackage [in]

A flag for whether this package is a default applicable package.


#### - inputStream [in]


            An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of <i>fileName</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9BB81F38-8451-4D3B-B0B6-31AF3001AB17">IAppxBundleWriter4</a>
 

 

