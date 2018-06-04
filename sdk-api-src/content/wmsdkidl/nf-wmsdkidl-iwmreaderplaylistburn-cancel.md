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

# IWMReaderPlaylistBurn::Cancel


## -description



The <b>Cancel</b> method cancels an initiated playlist burn before initialization is finished.




## -parameters






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



You should call this method to cancel the playlist burn process only after calling <a href="https://msdn.microsoft.com/a20a70af-49bc-408f-8c64-779525436f8d">InitPlaylistBurn</a> and before your status callback receives the WMT_INIT_PLAYLIST_BURN message. If you need to cancel the playlist burn after initialization is finished, you should call the <a href="https://msdn.microsoft.com/355f23eb-3cdb-4c27-bc48-499f349aef2b">EndPlaylistBurn</a> method and pass the E_ABORT error code.




## -see-also




<a href="https://msdn.microsoft.com/a0e1a4f3-4226-44a2-b38e-e5512fda2048">IWMReaderPlaylistBurn Interface</a>
 

 

