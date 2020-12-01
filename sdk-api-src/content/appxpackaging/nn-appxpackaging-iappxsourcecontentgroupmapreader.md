---
UID: NN:appxpackaging.IAppxSourceContentGroupMapReader
title: IAppxSourceContentGroupMapReader (appxpackaging.h)
description: Gets information about the source content group map.
helpviewer_keywords: ["IAppxSourceContentGroupMapReader","IAppxSourceContentGroupMapReader interface [App packaging and management]","IAppxSourceContentGroupMapReader interface [App packaging and management]","described","appxpackaging/IAppxSourceContentGroupMapReader","appxpkg.iappxsourcecontentgroupmapreader"]
old-location: appxpkg\iappxsourcecontentgroupmapreader.htm
tech.root: appxpkg
ms.assetid: EA0DF7E6-C4EF-4A58-A13F-EB3789239084
ms.date: 12/05/2018
ms.keywords: IAppxSourceContentGroupMapReader, IAppxSourceContentGroupMapReader interface [App packaging and management], IAppxSourceContentGroupMapReader interface [App packaging and management],described, appxpackaging/IAppxSourceContentGroupMapReader, appxpkg.iappxsourcecontentgroupmapreader
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
 - IAppxSourceContentGroupMapReader
 - appxpackaging/IAppxSourceContentGroupMapReader
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
 - IAppxSourceContentGroupMapReader
---

# IAppxSourceContentGroupMapReader interface


## -description

Gets information about the source content group map.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxSourceContentGroupMapReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxSourceContentGroupMapReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxSourceContentGroupMapReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxsourcecontentgroupmapreader-getautomaticgroups">GetAutomaticGroups</a>
</td>
<td align="left" width="63%">
Gets the automatic content group(s) from the source content group map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxsourcecontentgroupmapreader-getrequiredgroup">GetRequiredGroup</a>
</td>
<td align="left" width="63%">
Gets the required content group from the source content group map.

</td>
</tr>
</table>