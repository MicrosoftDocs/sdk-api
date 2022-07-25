---
UID: NF:appxpackaging.IAppxFactory2.CreateContentGroupMapReader
title: IAppxFactory2::CreateContentGroupMapReader (appxpackaging.h)
description: Creates an IAppxContentGroupMapReader.
helpviewer_keywords: ["CreateContentGroupMapReader","CreateContentGroupMapReader method [App packaging and management]","CreateContentGroupMapReader method [App packaging and management]","IAppxFactory2 interface","IAppxFactory2 interface [App packaging and management]","CreateContentGroupMapReader method","IAppxFactory2.CreateContentGroupMapReader","IAppxFactory2::CreateContentGroupMapReader","appxpackaging/IAppxFactory2::CreateContentGroupMapReader","appxpkg.iappxfactory2_createcontentgroupmapreader"]
old-location: appxpkg\iappxfactory2_createcontentgroupmapreader.htm
tech.root: appxpkg
ms.assetid: 42453BD7-AB65-49E0-86C0-4F96B4234397
ms.date: 12/05/2018
ms.keywords: CreateContentGroupMapReader, CreateContentGroupMapReader method [App packaging and management], CreateContentGroupMapReader method [App packaging and management],IAppxFactory2 interface, IAppxFactory2 interface [App packaging and management],CreateContentGroupMapReader method, IAppxFactory2.CreateContentGroupMapReader, IAppxFactory2::CreateContentGroupMapReader, appxpackaging/IAppxFactory2::CreateContentGroupMapReader, appxpkg.iappxfactory2_createcontentgroupmapreader
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxFactory2::CreateContentGroupMapReader
 - appxpackaging/IAppxFactory2::CreateContentGroupMapReader
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
 - IAppxFactory2.CreateContentGroupMapReader
---

# IAppxFactory2::CreateContentGroupMapReader


## -description

Creates an <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupmapreader">IAppxContentGroupMapReader</a>.

## -parameters

### -param inputStream [in]

The stream that delivers the content group map XML for reading.

### -param contentGroupMapReader [out, retval]

The content group map reader.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory2">IAppxFactory2</a>