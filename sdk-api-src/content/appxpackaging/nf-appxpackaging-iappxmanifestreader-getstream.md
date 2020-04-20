---
UID: NF:appxpackaging.IAppxManifestReader.GetStream
title: IAppxManifestReader::GetStream (appxpackaging.h)
description: Gets the raw XML parsed and read by the manifest reader.helpviewer_keywords: ["GetStream","GetStream method [App packaging and management]","GetStream method [App packaging and management]","IAppxManifestReader interface","IAppxManifestReader interface [App packaging and management]","GetStream method","IAppxManifestReader.GetStream","IAppxManifestReader::GetStream","appxpackaging/IAppxManifestReader::GetStream","appxpkg.iappxmanifestreader_getstream"]
old-location: appxpkg\iappxmanifestreader_getstream.htm
tech.root: appxpkg
ms.assetid: 00467E92-5282-4119-A036-00CE769839B9
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [App packaging and management], GetStream method [App packaging and management],IAppxManifestReader interface, IAppxManifestReader interface [App packaging and management],GetStream method, IAppxManifestReader.GetStream, IAppxManifestReader::GetStream, appxpackaging/IAppxManifestReader::GetStream, appxpkg.iappxmanifestreader_getstream
f1_keywords:
- appxpackaging/IAppxManifestReader.GetStream
dev_langs:
- c++
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- IAppxManifestReader.GetStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestReader::GetStream


## -description


Gets the raw XML parsed and read by the manifest reader.


## -parameters




### -param manifestStream [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

The read-only stream that represents the XML content of the manifest.




## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The raw XML stream is the entire source stream, and may contain elements and attributes in other namespaces that are ignored by the manifest reader.  For example, the XML stream may have elements in other namespaces that were marked in the <b>IgnorableNamespaces</b> attribute in the <b>Package</b> element, which were not validated. Therefore, you should consider this XML as untrusted. 

It is recommended that you use the packaging API to get information from the manifest, rather than parsing the raw XML.

If you parse the XML, you must include XML data validation and XML security testing.

Call the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when you have finished using the <i>manifestStream</i> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>
 

 

