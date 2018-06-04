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

# IWMPGraphCreation::GetGraphCreationFlags


## -description



One of the flags documented on this page is available in Windows Media Player 10 and Windows Media Player 11 running on Microsoft Windows XP. It might not be available in subsequent versions.
        



The <b>GetGraphCreationFlags</b> method is called by Windows Media Player to retrieve a value that represents the graph creation preferences.


## -parameters




### -param pdwFlags [out]

Address of a <b>DWORD</b> variable that receives a value that represents one or more graph creation flags combined by using bitwise OR operations.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
</table>
 




## -remarks



The following table describes the graph creation flags.

<table>
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>WMPGC_FLAGS_ALLOW_PREROLL</td>
<td>0x1</td>
<td>Windows Media Player will build the filter graph for the next media item before the current media item finishes playing.</td>
</tr>
<tr>
<td>WMPGC_FLAGS_SUPPRESS_DIALOGS</td>
<td>0x2</td>
<td>Windows Media Player will not display warning dialog boxes when errors occur.</td>
</tr>
<tr>
<td>WMPGC_FLAGS_IGNORE_AV_SYNC</td>
<td>0x4</td>
<td>
					Windows Media Player will not require audio and video to be synchronized when playing Windows Media-based content (.asf, .wma, or .wmv). Windows Media Player will attempt to play every frame of video. This occurs even when video data is arriving more slowly than audio data. 
					<div class="alert"><b>Note</b>  This flag is supported only in Windows Media Player 10 or 11 running on Microsoft Windows XP.</div>
<div> </div>
</td>
</tr>
<tr>
<td>WMPGC_FLAGS_DISABLE_PLUGINS</td>
<td>0x8</td>
<td>Disables all plug-ins for the current instance of the Windows Media Player control. This includes plug-ins native to Windows Media Player. For example, visualizations will not work when this flag is set.</td>
</tr>
<tr>
<td>WMPGC_FLAGS_USE_CUSTOM_GRAPH</td>
<td>0x10</td>
<td>Windows Media Player will use the application-provided DirectShow graph as-is and not attempt to further render the originally requested URL or file. Plug-ins will still be added to the custom graph unless the <b>WMPGC_FLAGS_DISABLE_PLUGINS</b> flag is also set. Set both these flags if you want WMP to use the provided graph without any changes. Requires Windows Media Player 12.</td>
</tr>
</table>
 

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/80d6f1f0-10c9-4e60-9bb7-556e340730a8">IWMPGraphCreation Interface</a>
 

 

