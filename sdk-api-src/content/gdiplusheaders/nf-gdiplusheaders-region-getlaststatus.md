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

# Region::GetLastStatus


## -description


The <b>Region::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>
 object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

The <b>Region::GetLastStatus</b> method returns an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>
 object have failed since the previous call to <b>Region::GetLastStatus</b>, then <b>Region::GetLastStatus</b> returns <b>Ok</b>.

If at least one method invoked on this 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>
 object has failed since the previous call to <b>Region::GetLastStatus</b>, then <b>Region::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>Region::GetLastStatus</b> immediately after constructing a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>
 object to determine whether the constructor succeeded.

The first time you call the <b>Region::GetLastStatus</b> method of a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>
 object, it returns <b>Ok</b> if the constructor succeeded and all methods invoked so far on the 
				<b>Region</b>
 object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a region from a path. Next, the code calls <a href="https://msdn.microsoft.com/20e6f834-1f36-4de0-b574-b89ebce917de">Region::GetBounds Methods</a>, followed by a call to <a href="https://msdn.microsoft.com/748cbc1c-cf0c-461f-ac14-52cf882a33b4">Region::GetDataSize</a>. The code then calls <b>Region::GetLastStatus</b>. If all method calls have been successful up to this point, <b>Region::GetLastStatus</b> returns <b>Ok</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetLastStatus(HDC hdc)
{
   Graphics graphics(hdc);

   Point points[] = {
      Point(110, 20),
      Point(120, 30),
      Point(100, 60),
      Point(120, 70),
      Point(150, 60),
      Point(140, 10)};

   Rect rect;
   UINT size;
   GraphicsPath path;

   path.AddClosedCurve(points, 6);

   // Create a region from a path.
   Region pathRegion(&amp;path);    

   pathRegion.GetBounds(&amp;rect, &amp;graphics);
   size = pathRegion.GetDataSize();

   if(pathRegion.GetLastStatus() == Ok)
   {
       // All methods called thus far have been successful.
   }
}</pre>
</td>
</tr>
</table></span></div>


