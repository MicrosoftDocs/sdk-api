---
UID: NF:appxpackaging.IAppxBundleManifestReader.GetStream
title: IAppxBundleManifestReader::GetStream (appxpackaging.h)
description: Gets the raw XML document without any preprocessing.
helpviewer_keywords: ["GetStream","GetStream method [App packaging and management]","GetStream method [App packaging and management]","IAppxBundleManifestReader interface","IAppxBundleManifestReader interface [App packaging and management]","GetStream method","IAppxBundleManifestReader.GetStream","IAppxBundleManifestReader::GetStream","appxpackaging/IAppxBundleManifestReader::GetStream","appxpkg.iappxbundlemanifestreader_getstream"]
old-location: appxpkg\iappxbundlemanifestreader_getstream.htm
tech.root: appxpkg
ms.assetid: DC276734-3837-466E-ADBA-60B68356504E
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [App packaging and management], GetStream method [App packaging and management],IAppxBundleManifestReader interface, IAppxBundleManifestReader interface [App packaging and management],GetStream method, IAppxBundleManifestReader.GetStream, IAppxBundleManifestReader::GetStream, appxpackaging/IAppxBundleManifestReader::GetStream, appxpkg.iappxbundlemanifestreader_getstream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxBundleManifestReader::GetStream
 - appxpackaging/IAppxBundleManifestReader::GetStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleManifestReader.GetStream
---

# IAppxBundleManifestReader::GetStream


## -description

Gets the raw XML document without any preprocessing.

## -parameters

### -param manifestStream [out, retval]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

The read-only stream that represents the XML content of the manifest.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The raw XML stream is the entire source stream and might contain elements and attributes in other namespaces that are ignored by the manifest reader.  For example, the XML stream might have elements in other namespaces that were marked in the <b>IgnorableNamespaces</b> attribute in the <b>Package</b> element, which were not validated. So, we recommend not to trust or parse this XML without security testing.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestreader">IAppxBundleManifestReader</a>