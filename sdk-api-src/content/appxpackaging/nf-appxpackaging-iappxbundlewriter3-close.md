---
UID: NF:appxpackaging.IAppxBundleWriter3.Close
title: IAppxBundleWriter3::Close (appxpackaging.h)
description: Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream. (IAppxBundleWriter3.Close)
helpviewer_keywords: ["Close","Close method [App packaging and management]","Close method [App packaging and management]","IAppxBundleWriter3 interface","IAppxBundleWriter3 interface [App packaging and management]","Close method","IAppxBundleWriter3.Close","IAppxBundleWriter3::Close","appxpackaging/IAppxBundleWriter3::Close","appxpkg.iappxbundlewriter3_close"]
old-location: appxpkg\iappxbundlewriter3_close.htm
tech.root: appxpkg
ms.assetid: 7AD526CD-9FF2-4A2A-BD12-21A0A9E1BA6E
ms.date: 12/05/2018
ms.keywords: Close, Close method [App packaging and management], Close method [App packaging and management],IAppxBundleWriter3 interface, IAppxBundleWriter3 interface [App packaging and management],Close method, IAppxBundleWriter3.Close, IAppxBundleWriter3::Close, appxpackaging/IAppxBundleWriter3::Close, appxpkg.iappxbundlewriter3_close
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
 - IAppxBundleWriter3::Close
 - appxpackaging/IAppxBundleWriter3::Close
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
 - IAppxBundleWriter3.Close
---

# IAppxBundleWriter3::Close


## -description

Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.

## -parameters

### -param hashMethodString [in]

The string value of the <b>HashMethod</b> attribute of the <a href="/uwp/schemas/blockmapschema/element-blockmap">BlockMap</a> root element.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter3">IAppxBundleWriter3</a>
