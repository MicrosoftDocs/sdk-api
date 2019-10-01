---
UID: NN:appxpackaging.IAppxFilesEnumerator
title: IAppxFilesEnumerator (appxpackaging.h)
author: windows-sdk-content
description: Enumerates the payload files in a package.
old-location: appxpkg\iappxfilesenumerator.htm
tech.root: appxpkg
ms.assetid: A9BB3242-5CDA-49A9-8A7B-5A9A3E31B724
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxFilesEnumerator, IAppxFilesEnumerator interface [App packaging and management], IAppxFilesEnumerator interface [App packaging and management],described, appxpackaging/IAppxFilesEnumerator, appxpkg.iappxfilesenumerator
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxFilesEnumerator"
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
 - IAppxFilesEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxFilesEnumerator interface


## -description


Enumerates the payload files in a package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxFilesEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxFilesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxFilesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfilesenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the payload file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfilesenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a payload file at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxfilesenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next payload file.

</td>
</tr>
</table> 


## -remarks



To get the footprint files, use the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile">IAppxPackageReader::GetFootprintFile</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfile">IAppxFile</a>
 

 

