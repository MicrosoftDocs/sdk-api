---
UID: NF:appxpackaging.IAppxBundleManifestReader.GetPackageInfoItems
title: IAppxBundleManifestReader::GetPackageInfoItems
author: windows-sdk-content
description: Retrieves an enumerator over all the &lt;Package&gt; elements under the &lt;Packages&gt; element.
old-location: appxpkg\iappxbundlemanifestreader_getpackageinfoitems.htm
tech.root: appxpkg
ms.assetid: D216C27E-5B73-49B5-90A8-11187C129264
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetPackageInfoItems, GetPackageInfoItems method [App packaging and management], GetPackageInfoItems method [App packaging and management],IAppxBundleManifestReader interface, IAppxBundleManifestReader interface [App packaging and management],GetPackageInfoItems method, IAppxBundleManifestReader.GetPackageInfoItems, IAppxBundleManifestReader::GetPackageInfoItems, appxpackaging/IAppxBundleManifestReader::GetPackageInfoItems, appxpkg.iappxbundlemanifestreader_getpackageinfoitems
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAppxBundleManifestReader.GetPackageInfoItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- appxpackaging.h
: 
- IAppxBundleManifestReader.GetPackageInfoItems
: 
---

# IAppxBundleManifestReader::GetPackageInfoItems


## -description


Retrieves an enumerator over all the &lt;Package&gt; elements under the &lt;Packages&gt; element. 


## -parameters




### -param packageInfoItems [out, retval]

Type: <b>IAppxBundleManifestPackageInfoEnumerator**</b>

 An enumerator over all payload packages in a &lt;Packages&gt; element of a bundle. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2ABC7B5A-6489-4B52-B1C4-22D432EC9947">IAppxBundleManifestReader</a>
 

 

