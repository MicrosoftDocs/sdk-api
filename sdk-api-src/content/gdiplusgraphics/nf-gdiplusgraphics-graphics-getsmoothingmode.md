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

# Graphics::GetSmoothingMode


## -description


The <b>Graphics::GetSmoothingMode</b> method determines whether smoothing (antialiasing) is applied to the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/42b3fc67-2cdb-4e14-88a0-aac914e8336a">SmoothingMode</a></b>
</strong>

If smoothing (antialiasing) is applied to this 
						<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object, this method returns SmoothingModeAntiAlias. If smoothing (antialiasing) is not applied to this 
						<b>Graphics</b> object, this method returns SmoothingModeNone. SmoothingModeAntiAlias and SmoothingModeNone are elements of the 
						<a href="https://msdn.microsoft.com/42b3fc67-2cdb-4e14-88a0-aac914e8336a">SmoothingMode</a> enumeration.




## -remarks



To get the rendering quality level for text, use the 
				<a href="https://msdn.microsoft.com/6525ac0e-bfd7-4471-bedb-df970b208222">Graphics::GetTextRenderingHint</a> method.


#### Examples



The following example sets the smoothing mode to high speed and draws an ellipse. It then gets the smoothing mode, changes it to high quality, and draws a second ellipse to demonstrate the difference.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetSmoothingMode(HDC hdc)
{
   Graphics graphics(hdc);

   // Set the smoothing mode to SmoothingModeHighSpeed.
   graphics.SetSmoothingMode(SmoothingModeHighSpeed);

   // Draw an ellipse.
   graphics.DrawEllipse(&amp;Pen(Color(255, 0, 0, 0), 3), Rect(10, 0, 200, 100));

   // Get the smoothing mode.
   SmoothingMode mode = graphics.GetSmoothingMode();


   // Test mode to see whether smoothing has been set for the Graphics object.
   if (mode == SmoothingModeAntiAlias)
   {
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   }

   // Draw an ellipse to demonstrate the difference.
   graphics.DrawEllipse(&amp;Pen(Color::Red, 3), Rect(220, 0, 200, 100));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7c4869c1-76ff-42d1-abf1-387121943b2a">Antialiasing with Lines and Curves</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>
 

 

