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

# IWMPPlayerServices::setTaskPaneURL


## -description




          This page documents a feature of the Windows Media Player 9 Series SDK and the Windows Media Player 10 SDK. It may be unavailable in subsequent versions.
        



The <b>setTaskPaneURL</b> method displays the specified URL in the specified task pane of the full mode of Windows Media Player.


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
<td>MediaGuide</td>
<td>Opens Windows Media Player in the <b>MediaGuide</b> feature.</td>
</tr>
<tr>
<td>RadioTuner</td>
<td>Opens Windows Media Player in the <b>RadioTuner</b> feature.</td>
</tr>
<tr>
<td>Services</td>
<td>Opens Windows Media Player in the <b>Premium Services</b> feature.</td>
</tr>
</table>
 


### -param bstrURL [in]

<b>BSTR</b> containing the URL to display in the task pane.


### -param bstrFriendlyName [in]

<b>BSTR</b> containing the friendly name of the content at the specified URL.


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



This method is used only when remoting the Windows Media Player control. This method must be called when the control is in the docked state. Once set, the specified task pane is opened the next time the remoted control transitions to Windows Media Player.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/3d9ca91f-c672-4ecb-a6db-67d7e1ddbe7e">IWMPPlayerServices Interface</a>



<a href="https://msdn.microsoft.com/4b34ec95-d9a3-4135-b369-39955199ac00">IWMPPlayerServices::setTaskPane</a>



<a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>
 

 

