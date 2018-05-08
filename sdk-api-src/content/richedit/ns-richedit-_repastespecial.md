---
UID: NS:richedit._repastespecial
title: "_repastespecial"
author: windows-driver-content
description: Contains information identifying whether the display aspect of a pasted object should be based on the content of the object or the icon that represent the object.
old-location: controls\REPASTESPECIAL.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\repastespecial.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: DVASPECT_CONTENT, DVASPECT_ICON, REPASTESPECIAL, REPASTESPECIAL structure [Windows Controls], _repastespecial, _win32_REPASTESPECIAL_str, _win32_REPASTESPECIAL_str_cpp, controls.REPASTESPECIAL, controls._win32_REPASTESPECIAL_str, richedit/REPASTESPECIAL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REPASTESPECIAL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Richedit.h
api_name:
-	REPASTESPECIAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

