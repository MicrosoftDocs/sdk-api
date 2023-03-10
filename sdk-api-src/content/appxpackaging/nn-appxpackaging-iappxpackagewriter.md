---
UID: NN:appxpackaging.IAppxPackageWriter
title: IAppxPackageWriter (appxpackaging.h)
description: Provides a write-only object model for app packages. (IAppxPackageWriter)
helpviewer_keywords: ["IAppxPackageWriter","IAppxPackageWriter interface [App packaging and management]","IAppxPackageWriter interface [App packaging and management]","described","appxpackaging/IAppxPackageWriter","appxpkg.iappxpackagewriter"]
old-location: appxpkg\iappxpackagewriter.htm
tech.root: appxpkg
ms.assetid: 097B7451-9A54-4C39-8F83-16DB49691B42
ms.date: 12/05/2018
ms.keywords: IAppxPackageWriter, IAppxPackageWriter interface [App packaging and management], IAppxPackageWriter interface [App packaging and management],described, appxpackaging/IAppxPackageWriter, appxpkg.iappxpackagewriter
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
 - IAppxPackageWriter
 - appxpackaging/IAppxPackageWriter
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
 - IAppxPackageWriter
---

# IAppxPackageWriter interface


## -description

Provides a write-only object model for app packages.

## -inheritance

The <b>IAppxPackageWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxPackageWriter</b> also has these types of members:

## -remarks

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createpackagewriter">CreatePackageWriter</a> method of the <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a> interface.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-create-a-package">How to create an app package</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>
