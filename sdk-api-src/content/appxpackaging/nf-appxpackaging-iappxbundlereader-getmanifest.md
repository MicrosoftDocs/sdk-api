---
UID: NF:appxpackaging.IAppxBundleReader.GetManifest
title: IAppxBundleReader::GetManifest (appxpackaging.h)
description: Retrieves a read-only manifest object from the bundle.
helpviewer_keywords: ["GetManifest","GetManifest method [App packaging and management]","GetManifest method [App packaging and management]","IAppxBundleReader interface","IAppxBundleReader interface [App packaging and management]","GetManifest method","IAppxBundleReader.GetManifest","IAppxBundleReader::GetManifest","appxpackaging/IAppxBundleReader::GetManifest","appxpkg.iappxbundlereader_getmanifest"]
old-location: appxpkg\iappxbundlereader_getmanifest.htm
tech.root: appxpkg
ms.assetid: C9D80910-8609-45D9-A3EC-05A033A36A4F
ms.date: 12/05/2018
ms.keywords: GetManifest, GetManifest method [App packaging and management], GetManifest method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetManifest method, IAppxBundleReader.GetManifest, IAppxBundleReader::GetManifest, appxpackaging/IAppxBundleReader::GetManifest, appxpkg.iappxbundlereader_getmanifest
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
 - IAppxBundleReader::GetManifest
 - appxpackaging/IAppxBundleReader::GetManifest
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
 - IAppxBundleReader.GetManifest
---

# IAppxBundleReader::GetManifest


## -description

Retrieves a read-only manifest object from the bundle.

## -parameters

### -param manifestReader [out, retval]

Type: <b>IAppxBundleManifestReader**</b>

The object model of the bundle manifest.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlereader">IAppxBundleReader</a>