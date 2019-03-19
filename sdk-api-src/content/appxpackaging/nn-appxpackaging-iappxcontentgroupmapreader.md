---
UID: NN:appxpackaging.IAppxContentGroupMapReader
title: IAppxContentGroupMapReader (appxpackaging.h)
author: windows-sdk-content
description: Gets information about a content group map.
old-location: appxpkg\iappxcontentgroupmapreader.htm
tech.root: appxpkg
ms.assetid: 45C6F61E-8CF6-4188-9715-3954562F8AB0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAppxContentGroupMapReader, IAppxContentGroupMapReader interface [App packaging and management], IAppxContentGroupMapReader interface [App packaging and management],described, appxpackaging/IAppxContentGroupMapReader, appxpkg.iappxcontentgroupmapreader
ms.topic: interface
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
 - IAppxContentGroupMapReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxContentGroupMapReader interface


## -description


Gets information about a content group map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxContentGroupMapReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxContentGroupMapReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxContentGroupMapReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3A5FE3A2-8D0D-4073-94FE-B0AC5DBF2D25">GetAutomaticGroups</a>
</td>
<td align="left" width="63%">
Gets the automatic content group(s) from the content group map.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45E4193E-EB4C-4D3D-989A-7AE35FDC2C77">GetRequiredGroup</a>
</td>
<td align="left" width="63%">
Gets the required content group from the content group map.

</td>
</tr>
</table> 

