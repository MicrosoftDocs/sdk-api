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

# IWMReaderPlaylistBurn::InitPlaylistBurn


## -description



The <b>InitPlaylistBurn</b> method initiates the playlist burning process, by checking the files in the playlist to ensure that they are licensed for copying as part of a playlist.




## -parameters




### -param cFiles [in]

Number of files in the playlist. This is also the number of members in the array of file names referenced by <i>pwszFilenames</i>.


### -param ppwszFilenames




### -param pCallback [in]

Address of the <b>IWMStatusCallback</b> implementation that will receive the WMT_INIT_PLAYLIST_BURN status message.


### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback. You can use this parameter to differentiate between messages from different objects when sharing a single status callback.


#### - pwszFilenames [in]

Address of an array of <b>WCHAR</b> strings. Each string contains the name of a file in the playlist. You must maintain the file order exactly as it exists in the playlist.


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



This method executes asynchronously. When it is finished, a WMT_INIT_PLAYLIST_BURN message is sent to the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">OnStatus</a> method of the <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a> interface identified by the <i>pCallback</i> parameter.

The files are checked to determine whether they are DRM-protected. If a file is protected, its license is checked to verify that the license allows copying to CD as part of a playlist.




## -see-also




<a href="https://msdn.microsoft.com/a0e1a4f3-4226-44a2-b38e-e5512fda2048">IWMReaderPlaylistBurn Interface</a>
 

 

