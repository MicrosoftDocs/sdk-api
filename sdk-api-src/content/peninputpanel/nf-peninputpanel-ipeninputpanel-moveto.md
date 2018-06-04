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

# IPenInputPanel::MoveTo


## -description



Deprecated.  The <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> has been replaced by the <a href="https://msdn.microsoft.com/867f2d6f-e63a-4c02-9370-3848a3b5c40a">Text Input Panel (TIP)</a>.

Sets the position of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object to a static screen position.




## -parameters




### -param Left [in]

 The new horizontal position in screen coordinates.


### -param Top [in]

The new vertical position in screen coordinates.


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



The <b>MoveTo</b> method causes an error if the control to which the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> is attached does not have focus. This method can be safely called if the pen input panel is not visible, as long as the attached control has focus.

If the new position causes the panel to appear outside the boundary of the screen working area, the panel is shifted toward the center of the working area so that the edges of the panel are adjacent to the nearest edges of the screen.

To explicitly override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object, use the <a href="https://msdn.microsoft.com/99af3767-5bc9-43e3-9413-5886f057cb85">Left</a> and <a href="https://msdn.microsoft.com/718263ae-d6ba-47ec-a18b-50488480b599">Top</a> properties of the <b>PenInputPanel</b> object to determine its current position. If the <b>PenInputPanel</b> is located on a section of the screen that should be visible, use the <b>MoveTo</b> method to relocate the <b>PenInputPanel</b>.

You can also override the automatic positioning behavior of the <a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a> object by monitoring to the <a href="https://msdn.microsoft.com/99af3767-5bc9-43e3-9413-5886f057cb85">Left</a> and <a href="https://msdn.microsoft.com/718263ae-d6ba-47ec-a18b-50488480b599">Top</a> parameters passed to a <a href="https://msdn.microsoft.com/0c51d875-cef9-4087-b17d-5c5af04f81a5">PanelMoving</a> event handler. If the <b>PenInputPanel</b> is located on a section of the screen that should be visible, use the <b>MoveTo</b> method to relocate the <b>PenInputPanel</b>.




## -see-also




<a href="tablet.ipeninputpanel">IPenInputPanel</a>



<a href="https://msdn.microsoft.com/ad63302e-b386-4b32-95bf-be1129839c33">PenInputPanel</a>
 

 

