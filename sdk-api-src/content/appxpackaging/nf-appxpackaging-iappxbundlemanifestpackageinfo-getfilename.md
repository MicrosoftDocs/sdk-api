---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetFileName
title: IAppxBundleManifestPackageInfo::GetFileName (appxpackaging.h)
author: windows-sdk-content
description: Retrieves the file-name attribute of the package.
old-location: appxpkg\iappxbundlemanifestpackageinfo_getfilename.htm
tech.root: appxpkg
ms.assetid: D8E827D4-0256-4598-A99A-EDB5FA14EDC2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFileName, GetFileName method [App packaging and management], GetFileName method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetFileName method, IAppxBundleManifestPackageInfo.GetFileName, IAppxBundleManifestPackageInfo::GetFileName, appxpackaging/IAppxBundleManifestPackageInfo::GetFileName, appxpkg.iappxbundlemanifestpackageinfo_getfilename
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
 - IAppxBundleManifestPackageInfo.GetFileName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleManifestPackageInfo::GetFileName


## -description


Retrieves the file-name attribute of the package.


## -parameters




### -param fileName [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

A string that contains the file name of the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can pass the package file name that  <b>GetFileName</b> outputs to the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlereader-getpayloadpackage">IAppxBundleReader::GetPayloadPackage</a> method to access the package’s contents.

When you're done using the file name, free the memory allocated for <i>fileName</i> by using the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo">IAppxBundleManifestPackageInfo</a>
 

 

