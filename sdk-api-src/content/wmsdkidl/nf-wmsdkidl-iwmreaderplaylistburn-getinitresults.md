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

# IWMReaderPlaylistBurn::GetInitResults


## -description



The <b>GetInitResults</b> method retrieves the results of the playlist file check.




## -parameters




### -param cFiles [in]

Number of files in the playlist. This is also the number of members in the array referenced by <i>phrStati</i>. This value must be the same as the number of files specified in the original call to <a href="https://msdn.microsoft.com/a20a70af-49bc-408f-8c64-779525436f8d">InitPlaylistBurn</a>.


### -param phrStati [out]

Address of an array of <b>HRESULT</b> values. The members of this array correspond to the file names passed in the original call to <b>InitPlaylistBurn</b>. On output, each member is set to S_OK if the corresponding file is approved for copying as part of the playlist. If a file in the playlist is not licensed for copying, or if an error is encountered, the corresponding member of this array is set to the appropriate <b>HRESULT</b> return code.


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



This method should be called in response to a WMT_INIT_PLAYLIST_BURN message received by your implementation of the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method. If you call <b>GetInitResults</b> without first calling <b>InitPlaylistBurn</b> and receiving the WMT_INIT_PLAYLIST_BURN message, <b>GetInitResults</b> will return an error code.

If, after calling this method, all members of the array referenced by <i>phrStati</i> are set to S_OK, you can begin copying the files in the playlist. However, you must use the same instance of the reader object for retrieving data that you used to get the <b>IWMReaderPlaylistBurn</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/a0e1a4f3-4226-44a2-b38e-e5512fda2048">IWMReaderPlaylistBurn Interface</a>
 

 

