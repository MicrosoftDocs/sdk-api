---
UID: NN:appxpackaging.IAppxFilesEnumerator
title: IAppxFilesEnumerator (appxpackaging.h)
description: Enumerates the payload files in a package.
helpviewer_keywords: ["IAppxFilesEnumerator","IAppxFilesEnumerator interface [App packaging and management]","IAppxFilesEnumerator interface [App packaging and management]","described","appxpackaging/IAppxFilesEnumerator","appxpkg.iappxfilesenumerator"]
old-location: appxpkg\iappxfilesenumerator.htm
tech.root: appxpkg
ms.assetid: A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724
ms.date: 12/05/2018
ms.keywords: IAppxFilesEnumerator, IAppxFilesEnumerator interface [App packaging and management], IAppxFilesEnumerator interface [App packaging and management],described, appxpackaging/IAppxFilesEnumerator, appxpkg.iappxfilesenumerator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxFilesEnumerator
 - appxpackaging/IAppxFilesEnumerator
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
 - IAppxFilesEnumerator
---

# IAppxFilesEnumerator interface


## -description

Enumerates the payload files in a package.

## -inheritance

The <b>IAppxFilesEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxFilesEnumerator</b> also has these types of members:

## -remarks

To get the footprint files, use the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile">IAppxPackageReader::GetFootprintFile</a> method.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>
