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

# _getcontextmenuex structure


## -description


Contains context menu information that is passed to the <a href="https://msdn.microsoft.com/760e0c36-f125-470d-b2eb-c72ed27611e1">IRichEditOleCallback::GetContextMenu</a> method.


## -struct-fields




### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The character-position range in the active display. 



### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

One or more of the following content menu flags: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GCMF_GRIPPER"></a><a id="gcmf_gripper"></a><dl>
<dt><b>GCMF_GRIPPER</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu that is invoked by tapping a touch gripper handle. 


</td>
</tr>
<tr>
<td width="40%"><a id="GCMF_SPELLING"></a><a id="gcmf_spelling"></a><dl>
<dt><b>GCMF_SPELLING</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu for a spelling error. 


</td>
</tr>
<tr>
<td width="40%"><a id="GCMF_MOUSEMENU"></a><a id="gcmf_mousemenu"></a><dl>
<dt><b>GCMF_MOUSEMENU</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu that is invoked by mouse.

</td>
</tr>
<tr>
<td width="40%"><a id="GCMF_TOUCHMENU"></a><a id="gcmf_touchmenu"></a><dl>
<dt><b>GCMF_TOUCHMENU</b></dt>
</dl>
</td>
<td width="60%">
Get the context menu that is invoked by touch. 


</td>
</tr>
</table>
 


### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The screen coordinates for the content menu. 


### -field pvReserved

Type: <b>void*</b>

Not used; must be zero.


## -see-also




<a href="https://msdn.microsoft.com/760e0c36-f125-470d-b2eb-c72ed27611e1">IRichEditOleCallback::GetContextMenu</a>
 

 

