---
UID: NN:appxpackaging.IAppxFactory2
title: IAppxFactory2 (appxpackaging.h)
description: Creates objects for reading and writing app packages.
old-location: appxpkg\iappxfactory2.htm
tech.root: appxpkg
ms.assetid: 01B11591-F854-4A39-8EDD-A5140235CA0B
ms.date: 12/05/2018
ms.keywords: IAppxFactory2, IAppxFactory2 interface [App packaging and management], IAppxFactory2 interface [App packaging and management],described, appxpackaging/IAppxFactory2, appxpkg.iappxfactory2
ms.topic: interface
f1_keywords:
- appxpackaging/IAppxFactory2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- AppxPackaging.h
api_name:
- IAppxFactory2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxFactory2 interface


## -description


Creates objects for reading and writing app packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFactory2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory2-createcontentgroupmapreader">CreateContentGroupMapReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupmapreader">IAppxContentGroupMapReader</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory2-createcontentgroupmapwriter">CreateContentGroupMapWriter</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupmapwriter">IAppxContentGroupMapWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfactory2-createsourcecontentgroupmapreader">CreateSourceContentGroupMapReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxsourcecontentgroupmapreader">IAppxSourceContentGroupMapReader</a>.

</td>
</tr>
</table> 

