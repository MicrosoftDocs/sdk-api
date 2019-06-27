---
UID: NN:appxpackaging.IAppxContentGroupsEnumerator
title: IAppxContentGroupsEnumerator (appxpackaging.h)
author: windows-sdk-content
description: Enumerates the content groups from a content group map.
old-location: appxpkg\iappxcontentgroupsenumerator.htm
tech.root: appxpkg
ms.assetid: BA91A1A6-6C6B-4086-AE95-47372581429C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxContentGroupsEnumerator, IAppxContentGroupsEnumerator interface [App packaging and management], IAppxContentGroupsEnumerator interface [App packaging and management],described, appxpackaging/IAppxContentGroupsEnumerator, appxpkg.iappxcontentgroupsenumerator
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxContentGroupsEnumerator"
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
 - IAppxContentGroupsEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxContentGroupsEnumerator interface


## -description


Enumerates the content groups from a content group map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxContentGroupsEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxContentGroupsEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxContentGroupsEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxcontentgroupsenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the content group at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxcontentgroupsenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a content group at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxcontentgroupsenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next content group.

</td>
</tr>
</table> 

