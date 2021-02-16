---
UID: NF:appxpackaging.IAppxBundleFactory.CreateBundleWriter
title: IAppxBundleFactory::CreateBundleWriter (appxpackaging.h)
description: Creates a write-only bundle object to which app packages can be added.
helpviewer_keywords: ["CreateBundleWriter","CreateBundleWriter method [App packaging and management]","CreateBundleWriter method [App packaging and management]","IAppxBundleFactory interface","IAppxBundleFactory interface [App packaging and management]","CreateBundleWriter method","IAppxBundleFactory.CreateBundleWriter","IAppxBundleFactory::CreateBundleWriter","appxpackaging/IAppxBundleFactory::CreateBundleWriter","appxpkg.iappxbundlefactory_createbundlewriter"]
old-location: appxpkg\iappxbundlefactory_createbundlewriter.htm
tech.root: appxpkg
ms.assetid: E77392FB-69A1-41B0-8B44-F05F126214E0
ms.date: 12/05/2018
ms.keywords: CreateBundleWriter, CreateBundleWriter method [App packaging and management], CreateBundleWriter method [App packaging and management],IAppxBundleFactory interface, IAppxBundleFactory interface [App packaging and management],CreateBundleWriter method, IAppxBundleFactory.CreateBundleWriter, IAppxBundleFactory::CreateBundleWriter, appxpackaging/IAppxBundleFactory::CreateBundleWriter, appxpkg.iappxbundlefactory_createbundlewriter
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
 - IAppxBundleFactory::CreateBundleWriter
 - appxpackaging/IAppxBundleFactory::CreateBundleWriter
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
 - IAppxBundleFactory.CreateBundleWriter
---

# IAppxBundleFactory::CreateBundleWriter


## -description

Creates a write-only bundle object to which app packages can be added.

## -parameters

### -param outputStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The output stream that receives the serialized package data. The stream must support at least the  <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">Write</a> method.

### -param bundleVersion [in]

Type: <b>UINT64</b>

The version number of the bundle.

 If set to 0, <b>CreateBundleWriter</b> sets the version number of the bundle to a value derived from the current system time.  We recommend passing 0 so version numbers are automatically generated and each successive call generates a higher version number.


For example, if you call <b>CreateBundleWriter</b> on 2013/12/23 3:45:00 AM UTC with <i>bundleVersion</i> set to 0, the version number of the bundle becomes 2013.1223.0345.0000.

### -param bundleWriter [out, retval]

Type: <b>IAppxBundleWriter**</b>

The bundle writer created by this method.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table.

## -remarks

Content added to the bundle is serialized out as an Appx bundle file to <i>outputStream</i>.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlefactory">IAppxBundleFactory</a>