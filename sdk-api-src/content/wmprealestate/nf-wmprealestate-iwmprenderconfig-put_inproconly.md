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

# IWMPRenderConfig::put_inProcOnly


## -description



The <b>put_inProcOnly</b> method specifies a value indicating whether playback is restricted to the current process.




## -parameters




### -param fInProc [in]

<b>BOOL</b>, <b>TRUE</b> specifying that playback is restricted to the current process.


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



Using this method with protected content is not supported.

This method can be helpful when debugging. If your program works with the Media Foundation topology directly (for example, specifying an EVR presenter by using the <a href="https://msdn.microsoft.com/60318e68-89dd-4505-a703-3de4d5442236">IWMPVideoRenderConfig</a> interface), it might be easier to debug your code when the presenter is in the same process.

This method might also be useful if your Media Foundation components are designed to run in the main program's process.

Note that DirectShow graphs in Windows Media Player always run in the main process.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/01a4c79e-9867-47c0-9aca-b2f1596f1c2a">IWMPRenderConfig Interface</a>
 

 

