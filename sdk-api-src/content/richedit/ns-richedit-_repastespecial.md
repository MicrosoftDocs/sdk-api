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

# _repastespecial structure


## -description


Contains information identifying whether the display aspect of a pasted object should be based on the content of the object or the icon that represent the object.


## -struct-fields




### -field dwAspect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Display aspect. It can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_CONTENT"></a><a id="dvaspect_content"></a><dl>
<dt><b>DVASPECT_CONTENT</b></dt>
</dl>
</td>
<td width="60%">
Aspect is based on the content of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_ICON"></a><a id="dvaspect_icon"></a><dl>
<dt><b>DVASPECT_ICON</b></dt>
</dl>
</td>
<td width="60%">
Aspect is based on the icon view of the object.

</td>
</tr>
</table>
 


### -field dwParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD_PTR</a></b>

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Aspect data. If <b>dwAspect</b> is DVASPECT_ICON, this member contains the handle to the metafile with the icon view of the object. 


## -see-also




<a href="https://msdn.microsoft.com/b4b9c1a7-943d-4dc8-bcb9-054c984b82ba">EM_PASTESPECIAL</a>
 

 

