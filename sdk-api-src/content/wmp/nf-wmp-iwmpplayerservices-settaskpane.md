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

# IWMPPlayerServices::setTaskPane


## -description



The <b>setTaskPane</b> method displays the specified task pane in the full mode of Windows Media Player.




## -parameters




### -param bstrTaskPane [in]

<b>BSTR</b> containing one of the following values.

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
<td>NowPlaying</td>
<td>
Windows Media Player 9, 10, 11: Opens Windows Media Player in the<b> Now Playing</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Player</b> mode .

</td>
</tr>
<tr>
<td>MediaGuide</td>
<td>
Windows Media Player 9, 10, 11: Opens Windows Media Player in the <b>Media Guide</b> feature. 

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the Media Guide displayed.

</td>
</tr>
<tr>
<td>CopyFromCD</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Copy From CD</b> feature.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Rip</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode.

</td>
</tr>
<tr>
<td>CopyFromCD?AutoCopy:<i>id</i></td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Copy From CD</b> feature and automatically invokes the copy functionality after switching.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Rip</b> feature and automatically invokes the rip functionality after switching.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode and automatically invokes the rip functionality after switching.

All versions: To specify a particular drive identifier, append a colon character (:) followed by the CD drive identifier number. If you omit the colon and the ID, the first CD drive is  used. If the user has selected <b>Eject CD when copying is completed</b> in Windows Media Player, the CD will be ejected when copying is completed.

</td>
</tr>
<tr>
<td>Library</td>
<td>
Windows Media Player 9, 10, 11: Opens Windows Media Player in the <b>Library</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the <b>Play</b> tab open.

</td>
</tr>
<tr>
<td>RadioTuner</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Radio Tuner</b> feature

Windows Media Player 10, 11, 12: Opens Windows Media Player in the current active online store.

</td>
</tr>
<tr>
<td>CopyToCD</td>
<td>
Windows Media Player 9: Not supported.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Burn</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the burn list open.

</td>
</tr>
<tr>
<td>CopyToCDOrDevice</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Copy to CD or Device</b> feature.

Windows Media Player 10, 11: Opens Windows Media Player in the <b>Sync</b> feature.

Windows Media Player 12: Opens Windows Media Player in <b>Library</b> mode with the <b>Sync</b> tab open.

</td>
</tr>
<tr>
<td>Services</td>
<td>
Windows Media Player 9: Opens Windows Media Player in the <b>Premium Services</b> feature 

Windows Media Player 10, 11, 12: Opens Windows Media Player in the current active online store.

</td>
</tr>
<tr>
<td>SkinChooser</td>
<td>
Opens Windows Media Player in the <b>Skin Chooser</b> feature.

</td>
</tr>
</table>
 


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



This method is used only when remoting the Windows Media Player control.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/4ceacaeb-09af-4cdf-84b7-04574a83ec48">IWMPPlayerServices::setTaskPaneURL(deprecated)</a>



<a href="https://msdn.microsoft.com/3d9ca91f-c672-4ecb-a6db-67d7e1ddbe7e">IWMPPlayerServicesInterface</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

