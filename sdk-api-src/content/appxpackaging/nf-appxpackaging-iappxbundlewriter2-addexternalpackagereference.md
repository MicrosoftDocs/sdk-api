---
UID: NF:appxpackaging.IAppxBundleWriter2.AddExternalPackageReference
title: IAppxBundleWriter2::AddExternalPackageReference (appxpackaging.h)
author: windows-sdk-content
description: Adds a reference to an external package to the package bundle.
old-location: appxpkg\iappxbundlewriter2_addexternalpackagereference.htm
tech.root: appxpkg
ms.assetid: 09297744-69E4-45D6-BA5C-A3B28130C6CC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddExternalPackageReference, AddExternalPackageReference method [App packaging and management], AddExternalPackageReference method [App packaging and management],IAppxBundleWriter2 interface, IAppxBundleWriter2 interface [App packaging and management],AddExternalPackageReference method, IAppxBundleWriter2.AddExternalPackageReference, IAppxBundleWriter2::AddExternalPackageReference, appxpackaging/IAppxBundleWriter2::AddExternalPackageReference, appxpkg.iappxbundlewriter2_addexternalpackagereference
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
 - IAppxBundleWriter2.AddExternalPackageReference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleWriter2::AddExternalPackageReference


## -description


Adds a reference to an external package to the package bundle.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param inputStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of <i>fileName</i>.
          The stream must support <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">Read</a>, <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/FD9EAF80-8449-4016-91A9-2299711C3D48">IAppxBundleWriter2</a>
 

 

