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

# IWMReaderAdvanced5::SetPlayerHook


## -description



The <b>SetPlayerHook</b> method assigns a player-hook callback to the reader. The reader calls the callback method before sending each sample to the graphics processor for decompression.




## -parameters




### -param dwOutputNum [in]

The output number to which the player-hook callback applies.


### -param pHook [in]

Pointer to the implementation of the <a href="https://msdn.microsoft.com/5e58cb6a-3398-4b12-881e-76f936f6c7b3">IWMPlayerHook</a> interface that will be used in association with the specified output.


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



DirectX Video Acceleration enables supported graphics cards to decompress video samples.




## -see-also




<a href="https://msdn.microsoft.com/28d697d8-99b5-4968-a765-ba01b86914f6">IWMReaderAdvanced5 Interface</a>
 

 

