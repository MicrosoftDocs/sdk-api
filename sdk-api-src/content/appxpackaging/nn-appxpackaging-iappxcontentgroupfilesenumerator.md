---
UID: NN:appxpackaging.IAppxContentGroupFilesEnumerator
title: IAppxContentGroupFilesEnumerator (appxpackaging.h)

description: Enumerates files in content groups from a content group map.
old-location: appxpkg\iappxcontentgroupfilesenumerator_.htm
tech.root: appxpkg
ms.assetid: 42F1E3DE-B2A3-42DE-8FBE-BEE02D546ABA

ms.date: 12/05/2018
ms.keywords: IAppxContentGroupFilesEnumerator, IAppxContentGroupFilesEnumerator interface [App packaging and management], IAppxContentGroupFilesEnumerator interface [App packaging and management],described, appxpackaging/IAppxContentGroupFilesEnumerator, appxpkg.iappxcontentgroupfilesenumerator_
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxContentGroupFilesEnumerator"
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
 - IAppxContentGroupFilesEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxContentGroupFilesEnumerator interface


## -description


Enumerates files in content groups from a content group map.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxContentGroupFilesEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxContentGroupFilesEnumerator</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactcollection-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the file from the content group at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxcontentgroupfilesenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxcontentgroupfilesenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next file.

</td>
</tr>
</table> 

