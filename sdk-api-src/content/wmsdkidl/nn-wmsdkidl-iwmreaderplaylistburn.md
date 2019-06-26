---
UID: NN:wmsdkidl.IWMReaderPlaylistBurn
title: IWMReaderPlaylistBurn (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderPlaylistBurn interface verifies that the files in a playlist can be copied to CD, in the order in which they are specified.
old-location: wmformat\iwmreaderplaylistburn.htm
tech.root: wmformat
ms.assetid: a0e1a4f3-4226-44a2-b38e-e5512fda2048
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderPlaylistBurn, IWMReaderPlaylistBurn interface [windows Media Format], IWMReaderPlaylistBurn interface [windows Media Format],described, IWMReaderPlaylistBurnInterface, wmformat.iwmreaderplaylistburn, wmsdkidl/IWMReaderPlaylistBurn
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMReaderPlaylistBurn"
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - wmsdkidl.h
api_name:
 - IWMReaderPlaylistBurn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderPlaylistBurn interface


## -description



The <b>IWMReaderPlaylistBurn</b> interface verifies that the files in a playlist can be copied to CD, in the order in which they are specified. If any of the files in the list are DRM-protected, the licenses are checked. DRM version 10 licenses track the number of times files are copied to CD as part of a playlist. The methods of this interface are intended to support applications that copy entire playlists to compact disc.

An <b>IWMReaderPlaylistBurn</b> interface exists for every instance of the reader object or synchronous reader object. You can get a pointer to the <b>IWMReaderPlaylistBurn</b> interface by calling the <b>QueryInterface</b> method of any other interface on one of those objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderPlaylistBurn</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderPlaylistBurn</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderPlaylistBurn</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels an initiated playlist burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn">EndPlaylistBurn</a>
</td>
<td align="left" width="63%">
Ends the playlist burning process, releasing any resources and updating counts for any DRM licenses involved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults">GetInitResults</a>
</td>
<td align="left" width="63%">
Retrieves the results of the playlist file check. This check is initiated by the <b>InitPlaylistBurn</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn">InitPlaylistBurn</a>
</td>
<td align="left" width="63%">
Starts the playlist file check.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

