---
UID: NN:wmsdkidl.IWMReaderPlaylistBurn
title: IWMReaderPlaylistBurn
author: windows-sdk-content
description: The IWMReaderPlaylistBurn interface verifies that the files in a playlist can be copied to CD, in the order in which they are specified.
old-location: wmformat\iwmreaderplaylistburn.htm
tech.root: wmformat
ms.assetid: a0e1a4f3-4226-44a2-b38e-e5512fda2048
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderPlaylistBurn, IWMReaderPlaylistBurn interface [windows Media Format], IWMReaderPlaylistBurn interface [windows Media Format],described, IWMReaderPlaylistBurnInterface, wmformat.iwmreaderplaylistburn, wmsdkidl/IWMReaderPlaylistBurn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IWMReaderPlaylistBurn interface


## -description



The <b>IWMReaderPlaylistBurn</b> interface verifies that the files in a playlist can be copied to CD, in the order in which they are specified. If any of the files in the list are DRM-protected, the licenses are checked. DRM version 10 licenses track the number of times files are copied to CD as part of a playlist. The methods of this interface are intended to support applications that copy entire playlists to compact disc.

An <b>IWMReaderPlaylistBurn</b> interface exists for every instance of the reader object or synchronous reader object. You can get a pointer to the <b>IWMReaderPlaylistBurn</b> interface by calling the <b>QueryInterface</b> method of any other interface on one of those objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderPlaylistBurn</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMReaderPlaylistBurn</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d126f13b-90ac-489e-8dd0-e507f4003a7a">Cancel</a>
</td>
<td align="left" width="63%">
Cancels an initiated playlist burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/355f23eb-3cdb-4c27-bc48-499f349aef2b">EndPlaylistBurn</a>
</td>
<td align="left" width="63%">
Ends the playlist burning process, releasing any resources and updating counts for any DRM licenses involved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f9db03b-0bcc-4442-b97e-f6a2f8d179fa">GetInitResults</a>
</td>
<td align="left" width="63%">
Retrieves the results of the playlist file check. This check is initiated by the <b>InitPlaylistBurn</b> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a20a70af-49bc-408f-8c64-779525436f8d">InitPlaylistBurn</a>
</td>
<td align="left" width="63%">
Starts the playlist file check.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

