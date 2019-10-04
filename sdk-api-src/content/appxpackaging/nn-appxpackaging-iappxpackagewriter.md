---
UID: NN:appxpackaging.IAppxPackageWriter
title: IAppxPackageWriter (appxpackaging.h)
author: windows-sdk-content
description: Provides a write-only object model for app packages.
old-location: appxpkg\iappxpackagewriter.htm
tech.root: appxpkg
ms.assetid: 097B7451-9A54-4C39-8F83-16DB49691B42
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxPackageWriter, IAppxPackageWriter interface [App packaging and management], IAppxPackageWriter interface [App packaging and management],described, appxpackaging/IAppxPackageWriter, appxpkg.iappxpackagewriter
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxPackageWriter"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxPackageWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxPackageWriter interface


## -description


Provides a write-only object model for app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxPackageWriter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxPackageWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxPackageWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile">AddPayloadFile</a>
</td>
<td align="left" width="63%">
Adds a new payload file to the app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagewriter-close">Close</a>
</td>
<td align="left" width="63%">
Writes footprint files at the end of the app package, and closes the package writer object's output stream.

</td>
</tr>
</table> 


## -remarks



This object can be retrieved using the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory-createpackagewriter">CreatePackageWriter</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfactory">IAppxFactory</a> interface.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/appxpkg/how-to-create-a-package">How to create an app package</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackagereader">IAppxPackageReader</a>
 

 

