---
UID: NF:appxpackaging.IAppxBundleWriter4.AddExternalPackageReference
title: IAppxBundleWriter4::AddExternalPackageReference
author: windows-sdk-content
description: Adds a reference within the package bundle to an external app package.
old-location: appxpkg\iappxbundlewriter4_addexternalpackagereference.htm
tech.root: appxpkg
ms.assetid: 2C655FF8-93F5-4132-8D61-1C47DB317043
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddExternalPackageReference, AddExternalPackageReference method [App packaging and management], AddExternalPackageReference method [App packaging and management],IAppxBundleWriter4 interface, IAppxBundleWriter4 interface [App packaging and management],AddExternalPackageReference method, IAppxBundleWriter4.AddExternalPackageReference, IAppxBundleWriter4::AddExternalPackageReference, appxpackaging/IAppxBundleWriter4::AddExternalPackageReference, appxpkg.iappxbundlewriter4_addexternalpackagereference
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
 - IAppxBundleWriter4.AddExternalPackageReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleWriter4::AddExternalPackageReference


## -description


Adds a reference within the package bundle to an external app package.


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
 

 

