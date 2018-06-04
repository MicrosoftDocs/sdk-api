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

# IWMPNetwork::get_downloadProgress


## -description



The <b>get_downloadProgress</b> method retrieves the percentage of the download completed.




## -parameters




### -param plDownloadProgress [out]

Pointer to a <b>long</b> containing the download progress.


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



When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the <b>get_downloadProgress</b> method retrieves the percentage of the total file that has been downloaded. This feature is currently supported only for digital media files downloaded from web servers. The following file formats can be downloaded and played simultaneously:

<ul>
<li>Advanced Systems Format (ASF)</li>
<li>Windows Media Audio (WMA)</li>
<li>Windows Media Video (WMV)</li>
<li>MP3</li>
<li>MPEG</li>
<li>WAV</li>
</ul>
In addition, some AVI files can be downloaded and played simultaneously.

Use the <b>IWMPEvents::Buffering</b> event to determine when buffering starts or stops.




## -see-also




<a href="https://msdn.microsoft.com/3e379c92-b400-48ad-a3d3-82ed3cd3f396">IWMPEvents::Buffering</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>
 

 

