---
UID: NN:appxpackaging.IAppxBundleWriter
title: IAppxBundleWriter (appxpackaging.h)

description: Provides a write-only object model for bundle packages.
old-location: appxpkg\iappxbundlewriter.htm
tech.root: appxpkg
ms.assetid: 5762E634-CBA6-496C-A771-CA5718E7E6AD

ms.date: 12/05/2018
ms.keywords: IAppxBundleWriter, IAppxBundleWriter interface [App packaging and management], IAppxBundleWriter interface [App packaging and management],described, appxpackaging/IAppxBundleWriter, appxpkg.iappxbundlewriter
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxBundleWriter"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBundleWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleWriter interface


## -description


Provides a write-only object model for bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleWriter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlewriter-addpayloadpackage">AddPayloadPackage</a>
</td>
<td align="left" width="63%">
Adds a new app package to the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlewriter-close">Close</a>
</td>
<td align="left" width="63%">
Finalizes the bundle package by writing footprint files at the end of the package, and closes the writer’s output stream.

</td>
</tr>
</table> 


## -remarks



You can use the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlefactory-createbundlewriter">CreateBundleWriter</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlefactory">IAppxBundleFactory</a> interface to retrieve the <b>IAppxBundleWriter</b> object. 

You can add only app packages to the writer.  The writer automatically generates footprint files, such as, the bundle’s manifest and block map.



