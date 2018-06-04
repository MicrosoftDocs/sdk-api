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

# NMPGCALCSIZE structure


## -description


Contains and receives information that the pager control uses to calculate the scrollable area of the contained window. It is used with the <a href="https://msdn.microsoft.com/a15f4191-2f26-4139-bdaf-bab219449b78">PGN_CALCSIZE</a> notification. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains information about the notification. 


### -field dwFlag

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Value that indicates which dimension is being requested. This will be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PGF_CALCHEIGHT"></a><a id="pgf_calcheight"></a><dl>
<dt><b>PGF_CALCHEIGHT</b></dt>
</dl>
</td>
<td width="60%">
The height of the scrollable area is being requested. The height must be placed in the 
						<b>iHeight</b> member before returning from the notification. 

</td>
</tr>
<tr>
<td width="40%"><a id="PGF_CALCWIDTH"></a><a id="pgf_calcwidth"></a><dl>
<dt><b>PGF_CALCWIDTH</b></dt>
</dl>
</td>
<td width="60%">
The width of the scrollable area is being requested. The width must be placed in the 
						<b>iWidth</b> member before returning from the notification. 

</td>
</tr>
</table>
 


### -field iWidth

Type: <b>int</b>

Receives the desired width of the scrollable area, in pixels. 


### -field iHeight

Type: <b>int</b>

Receives the desired height of the scrollable area, in pixels. 

