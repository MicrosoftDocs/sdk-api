---
UID: NF:appxpackaging.IAppxBundleReader.GetPayloadPackages
title: IAppxBundleReader::GetPayloadPackages (appxpackaging.h)
description: Retrieves an enumerator that iterates over the list of all payload packages in the bundle.
helpviewer_keywords: ["GetPayloadPackages","GetPayloadPackages method [App packaging and management]","GetPayloadPackages method [App packaging and management]","IAppxBundleReader interface","IAppxBundleReader interface [App packaging and management]","GetPayloadPackages method","IAppxBundleReader.GetPayloadPackages","IAppxBundleReader::GetPayloadPackages","appxpackaging/IAppxBundleReader::GetPayloadPackages","appxpkg.iappxbundlereader_getpayloadpackages"]
old-location: appxpkg\iappxbundlereader_getpayloadpackages.htm
tech.root: appxpkg
ms.assetid: 90C1CF98-D33F-4643-8978-7C74A4E5BD52
ms.date: 12/05/2018
ms.keywords: GetPayloadPackages, GetPayloadPackages method [App packaging and management], GetPayloadPackages method [App packaging and management],IAppxBundleReader interface, IAppxBundleReader interface [App packaging and management],GetPayloadPackages method, IAppxBundleReader.GetPayloadPackages, IAppxBundleReader::GetPayloadPackages, appxpackaging/IAppxBundleReader::GetPayloadPackages, appxpkg.iappxbundlereader_getpayloadpackages
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
 - IAppxBundleReader::GetPayloadPackages
 - appxpackaging/IAppxBundleReader::GetPayloadPackages
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
 - IAppxBundleReader.GetPayloadPackages
---

# IAppxBundleReader::GetPayloadPackages


## -description

Retrieves an enumerator that iterates over the list of all payload packages in the bundle.

## -parameters

### -param payloadPackages [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfilesenumerator">IAppxFilesEnumerator</a>**</b>

 An enumerator over all payload packages in the bundle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlereader">IAppxBundleReader</a>