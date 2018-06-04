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

# IWMReaderPlaylistBurn::EndPlaylistBurn


## -description



The <b>EndPlaylistBurn</b> method completes the playlist burn process. This includes releasing resources and adjusting counts associated with rights in DRM licenses.




## -parameters




### -param hrBurnResult [in]

Result of the playlist burn. Set to S_OK if the files in the playlist were successfully copied to CD. Otherwise, set to an appropriate <b>HRESULT</b> error code.


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



To abort the playlist burn process after your status callback receives the WMT_INIT_PLAYLIST_BURN message, pass the E_ABORT error code. To stop the process before initialization is complete, call the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a0e1a4f3-4226-44a2-b38e-e5512fda2048">IWMReaderPlaylistBurn Interface</a>
 

 

