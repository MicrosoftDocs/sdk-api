---
UID: NF:appxpackaging.IAppxBundleManifestReader.GetPackageId
title: IAppxBundleManifestReader::GetPackageId (appxpackaging.h)
author: windows-sdk-content
description: Retrieves an object that represents the &lt;Identity&gt; element under the root &lt;Bundle&gt; element.
old-location: appxpkg\iappxbundlemanifestreader_getpackageid.htm
tech.root: appxpkg
ms.assetid: B1D8AF8D-A80B-4F28-A9AA-A798D309D6E0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPackageId, GetPackageId method [App packaging and management], GetPackageId method [App packaging and management],IAppxBundleManifestReader interface, IAppxBundleManifestReader interface [App packaging and management],GetPackageId method, IAppxBundleManifestReader.GetPackageId, IAppxBundleManifestReader::GetPackageId, appxpackaging/IAppxBundleManifestReader::GetPackageId, appxpkg.iappxbundlemanifestreader_getpackageid
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
 - IAppxBundleManifestReader.GetPackageId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleManifestReader::GetPackageId


## -description


Retrieves an object that represents the &lt;Identity&gt; element under the root &lt;Bundle&gt; element. 


## -parameters




### -param packageId [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>**</b>

The package identifier.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>packageId</i> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestreader">IAppxBundleManifestReader</a>
 

 

