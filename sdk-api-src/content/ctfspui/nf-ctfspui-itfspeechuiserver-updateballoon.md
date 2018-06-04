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

# ITfSpeechUIServer::UpdateBalloon


## -description




## -parameters




### -param style [in]

Contains a <a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">TfLBBalloonStyle</a> element that specifies the balloon style.


### -param pch [in]

Pointer to a zero-terminated Unicode string that contains the text to show in the balloon.


### -param cch [in]

Specifies the number of characters in the string of the <i>pch</i> parameter.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/40961001-b659-4ddb-ae7d-5342957770be">ITfSpeechUIServer
      </a>



<a href="https://msdn.microsoft.com/c79eb490-b950-4d49-bdf9-821f3706446d">
        TfLBBalloonStyle
      </a>
 

 

