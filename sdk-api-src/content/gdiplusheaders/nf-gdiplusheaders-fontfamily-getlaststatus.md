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

# FontFamily::GetLastStatus


## -description


The <b>FontFamily::GetLastStatus</b> method returns a value that indicates the nature of this <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

The <b>FontFamily::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If no methods invoked on this <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object have failed since the previous call to <b>FontFamily::GetLastStatus</b>, then <b>FontFamily::GetLastStatus</b> returns Ok.

If at least one method invoked on this <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object has failed since the previous call to <b>FontFamily::GetLastStatus</b>, then <b>FontFamily::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>FontFamily::GetLastStatus</b> immediately after constructing a <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object to determine whether the constructor succeeded.

The first time you call the <b>FontFamily::GetLastStatus</b> method of a 
<a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the <b>FontFamily</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a> object and then checks the status of the call to create the object. If the call was successful, the example draws text.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetLastStatus(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a FontFamily object.
   FontFamily myFontFamily(L"arial");
   
   // Check the status of the last call.
   Status status = myFontFamily.GetLastStatus();

   // If the last call succeeded, draw text.
   if (status ==Ok)
   {
       SolidBrush solidbrush(Color(255, 0, 0, 0));
       Font       font(&amp;myFontFamily, 16);
       WCHAR      string[] = L"status = Ok";
       graphics.DrawString(string, -1, &amp;font, PointF(0, 0), &amp;solidbrush);
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/57428fae-6af4-47a5-a499-717dc378767a">Constructing Font Families and Fonts</a>



<a href="https://msdn.microsoft.com/cdd2ee9e-eb32-420f-8118-50582b55b7cd">FontFamily</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
 

 

