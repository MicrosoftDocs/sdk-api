---
UID: NN:appxpackaging.IAppxContentGroupFilesEnumerator
title: IAppxContentGroupFilesEnumerator
author: windows-sdk-content
description: Enumerates files in content groups from a content group map.
old-location: appxpkg\iappxcontentgroupfilesenumerator_.htm
tech.root: appxpkg
ms.assetid: 42F1E3DE-B2A3-42DE-8FBE-BEE02D546ABA
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAppxContentGroupFilesEnumerator, IAppxContentGroupFilesEnumerator interface [App packaging and management], IAppxContentGroupFilesEnumerator interface [App packaging and management],described, appxpackaging/IAppxContentGroupFilesEnumerator, appxpkg.iappxcontentgroupfilesenumerator_
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
 - IAppxContentGroupFilesEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxContentGroupFilesEnumerator interface


## -description


Enumerates files in content groups from a content group map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxContentGroupFilesEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxContentGroupFilesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxContentGroupFilesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff800917(v=VS.85).aspx">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the file from the content group at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCF7C214-74EF-4821-B293-D2D933560200">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39E27BFE-2383-4AB1-B83E-79573D87AAD6">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next file.

</td>
</tr>
</table> 

