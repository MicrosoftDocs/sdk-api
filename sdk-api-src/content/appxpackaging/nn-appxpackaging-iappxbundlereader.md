---
UID: NN:appxpackaging.IAppxBundleReader
title: IAppxBundleReader (appxpackaging.h)
description: Provides a read-only object model for bundle packages.
helpviewer_keywords: ["IAppxBundleReader","IAppxBundleReader interface [App packaging and management]","IAppxBundleReader interface [App packaging and management]","described","appxpackaging/IAppxBundleReader","appxpkg.iappxbundlereader"]
old-location: appxpkg\iappxbundlereader.htm
tech.root: appxpkg
ms.assetid: 3847AF32-D8E4-4BB2-9FBC-7CFAEF2CA664
ms.date: 12/05/2018
ms.keywords: IAppxBundleReader, IAppxBundleReader interface [App packaging and management], IAppxBundleReader interface [App packaging and management],described, appxpackaging/IAppxBundleReader, appxpkg.iappxbundlereader
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
 - IAppxBundleReader
 - appxpackaging/IAppxBundleReader
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
 - IAppxBundleReader
---

# IAppxBundleReader interface


## -description

Provides a read-only object model for bundle packages.

## -inheritance

The <b>IAppxBundleReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleReader</b> also has these types of members:

## -remarks

You can use the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlefactory-createbundlereader">CreateBundleReader</a> method of the <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlefactory">IAppxBundleFactory</a> interface to retrieve the <b>IAppxBundleReader</b> object. 

Through <b>IAppxBundleReader</b>, you can retrieve both footprint files, such as the bundle’s manifest, block map, and signature, and app packages that are contained in the bundle.
