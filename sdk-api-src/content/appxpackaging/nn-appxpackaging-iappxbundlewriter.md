---
UID: NN:appxpackaging.IAppxBundleWriter
title: IAppxBundleWriter (appxpackaging.h)
description: Provides a write-only object model for bundle packages. (IAppxBundleWriter)
helpviewer_keywords: ["IAppxBundleWriter","IAppxBundleWriter interface [App packaging and management]","IAppxBundleWriter interface [App packaging and management]","described","appxpackaging/IAppxBundleWriter","appxpkg.iappxbundlewriter"]
old-location: appxpkg\iappxbundlewriter.htm
tech.root: appxpkg
ms.assetid: 5762E634-CBA6-496C-A771-CA5718E7E6AD
ms.date: 12/05/2018
ms.keywords: IAppxBundleWriter, IAppxBundleWriter interface [App packaging and management], IAppxBundleWriter interface [App packaging and management],described, appxpackaging/IAppxBundleWriter, appxpkg.iappxbundlewriter
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
 - IAppxBundleWriter
 - appxpackaging/IAppxBundleWriter
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
 - IAppxBundleWriter
---

# IAppxBundleWriter interface


## -description

Provides a write-only object model for bundle packages.

## -inheritance

The <b>IAppxBundleWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleWriter</b> also has these types of members:

## -remarks

You can use the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlefactory-createbundlewriter">CreateBundleWriter</a> method of the <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlefactory">IAppxBundleFactory</a> interface to retrieve the <b>IAppxBundleWriter</b> object. 

You can add only app packages to the writer.  The writer automatically generates footprint files, such as, the bundle’s manifest and block map.
