---
UID: NF:appxpackaging.IAppxBundleManifestReader.GetStream
title: IAppxBundleManifestReader::GetStream
author: windows-sdk-content
description: Gets the raw XML document without any preprocessing.
old-location: appxpkg\iappxbundlemanifestreader_getstream.htm
old-project: appxpkg
ms.assetid: DC276734-3837-466E-ADBA-60B68356504E
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: GetStream, GetStream method [App packaging and management], GetStream method [App packaging and management],IAppxBundleManifestReader interface, IAppxBundleManifestReader interface [App packaging and management],GetStream method, IAppxBundleManifestReader.GetStream, IAppxBundleManifestReader::GetStream, appxpackaging/IAppxBundleManifestReader::GetStream, appxpkg.iappxbundlemanifestreader_getstream
ms.prod: windows
ms.technology: windows-sdk
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
 - IAppxBundleManifestReader.GetStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxBundleManifestReader::GetStream


## -description


Gets the raw XML document without any preprocessing.


## -parameters




### -param manifestStream [out, retval]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

The read-only stream that represents the XML content of the manifest.




## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The raw XML stream is the entire source stream and might contain elements and attributes in other namespaces that are ignored by the manifest reader.  For example, the XML stream might have elements in other namespaces that were marked in the <b>IgnorableNamespaces</b> attribute in the <b>Package</b> element, which were not validated. So, we recommend not to trust or parse this XML without security testing. 




## -see-also




<a href="https://msdn.microsoft.com/2ABC7B5A-6489-4B52-B1C4-22D432EC9947">IAppxBundleManifestReader</a>
 

 

