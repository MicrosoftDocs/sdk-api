---
UID: NF:appxpackaging.IAppxFactory2.CreateContentGroupMapWriter
title: IAppxFactory2::CreateContentGroupMapWriter (appxpackaging.h)
description: Creates an IAppxContentGroupMapWriter.
helpviewer_keywords: ["CreateContentGroupMapWriter","CreateContentGroupMapWriter method [App packaging and management]","CreateContentGroupMapWriter method [App packaging and management]","IAppxFactory2 interface","IAppxFactory2 interface [App packaging and management]","CreateContentGroupMapWriter method","IAppxFactory2.CreateContentGroupMapWriter","IAppxFactory2::CreateContentGroupMapWriter","appxpackaging/IAppxFactory2::CreateContentGroupMapWriter","appxpkg.iappxfactory2_createcontentgroupmapwriter"]
old-location: appxpkg\iappxfactory2_createcontentgroupmapwriter.htm
tech.root: appxpkg
ms.assetid: 4BFF656D-4B89-4D05-9A41-44400F75E8BC
ms.date: 12/05/2018
ms.keywords: CreateContentGroupMapWriter, CreateContentGroupMapWriter method [App packaging and management], CreateContentGroupMapWriter method [App packaging and management],IAppxFactory2 interface, IAppxFactory2 interface [App packaging and management],CreateContentGroupMapWriter method, IAppxFactory2.CreateContentGroupMapWriter, IAppxFactory2::CreateContentGroupMapWriter, appxpackaging/IAppxFactory2::CreateContentGroupMapWriter, appxpkg.iappxfactory2_createcontentgroupmapwriter
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
 - IAppxFactory2::CreateContentGroupMapWriter
 - appxpackaging/IAppxFactory2::CreateContentGroupMapWriter
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
 - IAppxFactory2.CreateContentGroupMapWriter
---

# IAppxFactory2::CreateContentGroupMapWriter


## -description

Creates an <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupmapwriter">IAppxContentGroupMapWriter</a>.

## -parameters

### -param stream

The stream that receives the content group map.

### -param contentGroupMapWriter [out, retval]

Provides a write-only object model for a content group map.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory2">IAppxFactory2</a>