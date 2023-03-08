---
UID: NF:appxpackaging.IAppxFactory2.CreateSourceContentGroupMapReader
title: IAppxFactory2::CreateSourceContentGroupMapReader (appxpackaging.h)
description: Creates an IAppxSourceContentGroupMapReader.
helpviewer_keywords: ["CreateSourceContentGroupMapReader","CreateSourceContentGroupMapReader method [App packaging and management]","CreateSourceContentGroupMapReader method [App packaging and management]","IAppxFactory2 interface","IAppxFactory2 interface [App packaging and management]","CreateSourceContentGroupMapReader method","IAppxFactory2.CreateSourceContentGroupMapReader","IAppxFactory2::CreateSourceContentGroupMapReader","appxpackaging/IAppxFactory2::CreateSourceContentGroupMapReader","appxpkg.iappxfactory2_createsourcecontentgroupmapreader"]
old-location: appxpkg\iappxfactory2_createsourcecontentgroupmapreader.htm
tech.root: appxpkg
ms.assetid: DB0FFB8D-A9DB-4B9C-B277-76623ECA3D6B
ms.date: 12/05/2018
ms.keywords: CreateSourceContentGroupMapReader, CreateSourceContentGroupMapReader method [App packaging and management], CreateSourceContentGroupMapReader method [App packaging and management],IAppxFactory2 interface, IAppxFactory2 interface [App packaging and management],CreateSourceContentGroupMapReader method, IAppxFactory2.CreateSourceContentGroupMapReader, IAppxFactory2::CreateSourceContentGroupMapReader, appxpackaging/IAppxFactory2::CreateSourceContentGroupMapReader, appxpkg.iappxfactory2_createsourcecontentgroupmapreader
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
 - IAppxFactory2::CreateSourceContentGroupMapReader
 - appxpackaging/IAppxFactory2::CreateSourceContentGroupMapReader
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
 - IAppxFactory2.CreateSourceContentGroupMapReader
---

# IAppxFactory2::CreateSourceContentGroupMapReader


## -description

Creates an <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxsourcecontentgroupmapreader">IAppxSourceContentGroupMapReader</a>.

## -parameters

### -param inputStream [in]

The stream that delivers the source content group map XML for reading.

### -param reader [out, retval]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory2">IAppxFactory2</a>