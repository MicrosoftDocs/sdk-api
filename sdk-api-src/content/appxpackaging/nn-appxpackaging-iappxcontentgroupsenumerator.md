---
UID: NN:appxpackaging.IAppxContentGroupsEnumerator
title: IAppxContentGroupsEnumerator
author: windows-sdk-content
description: Enumerates the content groups from a content group map.
old-location: appxpkg\iappxcontentgroupsenumerator.htm
old-project: appxpkg
ms.assetid: BA91A1A6-6C6B-4086-AE95-47372581429C
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IAppxContentGroupsEnumerator, IAppxContentGroupsEnumerator interface [App packaging and management], IAppxContentGroupsEnumerator interface [App packaging and management],described, appxpackaging/IAppxContentGroupsEnumerator, appxpkg.iappxcontentgroupsenumerator
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
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
req.lib: 
req.dll: 
req.irql: 
---

# IAppxContentGroupsEnumerator interface


## -description


Enumerates the content groups from a content group map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxContentGroupsEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxContentGroupsEnumerator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1A7055F5-6121-4A3A-AE7C-4BFDF6D7F1A9">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the content group at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5935EA6A-AD7F-4462-B539-A01439D0A373">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a content group at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/001F7B38-9588-4C87-9EC3-FB8D91959BB0">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next content group.

</td>
</tr>
</table> 

