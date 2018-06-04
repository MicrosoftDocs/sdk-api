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

# _imecomptext structure


## -description


Contains information about the Input Method Editor (IME) composition text in a Microsoft Rich Edit control.
		


## -struct-fields




### -field cb

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Size of the output buffer, in bytes. 


### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Type of composition string. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ICT_RESULTREADSTR"></a><a id="ict_resultreadstr"></a><dl>
<dt><b>ICT_RESULTREADSTR</b></dt>
</dl>
</td>
<td width="60%">
The final composed string.

</td>
</tr>
</table>
 


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/1516305c-5f87-4ae0-97db-8709c71abacc">EM_GETIMECOMPTEXT</a> message.




## -see-also




<a href="https://msdn.microsoft.com/1516305c-5f87-4ae0-97db-8709c71abacc">EM_GETIMECOMPTEXT</a>
 

 

