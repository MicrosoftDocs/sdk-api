---
UID: NN:appxpackaging.IAppxContentGroupMapWriter
title: IAppxContentGroupMapWriter (appxpackaging.h)
description: Provides a write-only object model for a content group map.
helpviewer_keywords: ["IAppxContentGroupMapWriter","IAppxContentGroupMapWriter interface [App packaging and management]","IAppxContentGroupMapWriter interface [App packaging and management]","described","appxpackaging/IAppxContentGroupMapWriter","appxpkg.iappxcontentgroupmapwriter"]
old-location: appxpkg\iappxcontentgroupmapwriter.htm
tech.root: appxpkg
ms.assetid: A9B3992C-D3D1-4190-9314-A21E388E88BA
ms.date: 12/05/2018
ms.keywords: IAppxContentGroupMapWriter, IAppxContentGroupMapWriter interface [App packaging and management], IAppxContentGroupMapWriter interface [App packaging and management],described, appxpackaging/IAppxContentGroupMapWriter, appxpkg.iappxcontentgroupmapwriter
f1_keywords:
- appxpackaging/IAppxContentGroupMapWriter
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
- IAppxContentGroupMapWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxContentGroupMapWriter interface


## -description


Provides a write-only object model for a content group map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxContentGroupMapWriter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxContentGroupMapWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxContentGroupMapWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxcontentgroupmapwriter-addautomaticfile">AddAutomaticFile</a>
</td>
<td align="left" width="63%">
Adds files to an automatic content group in a content group map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxcontentgroupmapwriter-addautomaticgroup">AddAutomaticGroup</a>
</td>
<td align="left" width="63%">
Adds an automatic content group to the content group map.

</td>
</tr>
</table> 

