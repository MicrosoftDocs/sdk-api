---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMPCore3::newPlaylist


## -description



The <b>newPlaylist</b> method retrieves a pointer to an <b>IWMPPlaylist</b> interface for a new playlist.




## -parameters




### -param bstrName [in]

<b>BSTR</b> containing the playlist name.


### -param bstrURL [in]

<b>BSTR</b> containing the playlist URL.


### -param ppPlaylist [out]

Pointer to a pointer to an <b>IWMPPlaylist</b> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If the <i>bstrURL</i> parameter is a null or empty string, this method creates an empty <b>Playlist</b> object. If the <i>bstrname</i> parameter is an empty string, this method applies the current metafile name.

The new playlist created with this method is not added to the library. To add a new playlist to the library, use <b>IWMPPlaylistCollection::importPlaylist</b> or <b>IWMPPlaylistCollection::newPlaylist</b>. Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.

Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.




## -see-also




<a href="https://msdn.microsoft.com/3004551e-ce36-4f15-88c3-93b2bfaa72fc">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/421a1bd3-65c1-4d8f-be75-918b1cfa06d2">IWMPPlaylistCollection::importPlaylist</a>



<a href="https://msdn.microsoft.com/5ad51469-a150-4322-ac16-782ef0d96a57">IWMPPlaylistCollection::newPlaylist</a>
 

 

