---
UID: NF:appxpackaging.IAppxBundleManifestOptionalBundleInfo.GetFileName
title: IAppxBundleManifestOptionalBundleInfo::GetFileName
author: windows-sdk-content
description: Retrieves the file-name attribute of the &lt;OptionalBundle&gt;.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfo_getfilename.htm
old-project: appxpkg
ms.assetid: 6553DAC3-D938-4653-8DE4-A5CA02640D31
ms.author: windowssdkdev
ms.date: 06/22/2018
ms.keywords: GetFileName, GetFileName method [App packaging and management], GetFileName method [App packaging and management],IAppxBundleManifestOptionalBundleInfo interface, IAppxBundleManifestOptionalBundleInfo interface [App packaging and management],GetFileName method, IAppxBundleManifestOptionalBundleInfo.GetFileName, IAppxBundleManifestOptionalBundleInfo::GetFileName, appxpackaging/IAppxBundleManifestOptionalBundleInfo::GetFileName, appxpkg.iappxbundlemanifestoptionalbundleinfo_getfilename
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
 - IAppxBundleManifestOptionalBundleInfo.GetFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestOptionalBundleInfo::GetFileName


## -description


Retrieves the file-name attribute of the &lt;OptionalBundle&gt;.


## -parameters




### -param fileName [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a>*</b>

A string that contains the file name of the package.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C9DC823D-46D5-4459-A20A-0969D20C6E9E">IAppxBundleManifestOptionalBundleInfo</a>
 

 

