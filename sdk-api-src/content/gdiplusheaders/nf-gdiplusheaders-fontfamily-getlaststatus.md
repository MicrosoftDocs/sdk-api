---
UID: NF:gdiplusheaders.FontFamily.GetLastStatus
title: FontFamily::GetLastStatus
author: windows-sdk-content
description: The FontFamily::GetLastStatus method returns a value that indicates the nature of this FontFamily object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetLastStatus_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getlaststatus_12.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FontFamily class [GDI+],GetLastStatus method, FontFamily.GetLastStatus, FontFamily::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetLastStatus_, gdiplus._gdiplus_CLASS_FontFamily_GetLastStatus_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - FontFamily.GetLastStatus
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# FontFamily::GetLastStatus


## -description


The <b>FontFamily::GetLastStatus</b> method returns a value that indicates the nature of this <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

The <b>FontFamily::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If no methods invoked on this <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object have failed since the previous call to <b>FontFamily::GetLastStatus</b>, then <b>FontFamily::GetLastStatus</b> returns Ok.

If at least one method invoked on this <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object has failed since the previous call to <b>FontFamily::GetLastStatus</b>, then <b>FontFamily::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>FontFamily::GetLastStatus</b> immediately after constructing a <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object to determine whether the constructor succeeded.

The first time you call the <b>FontFamily::GetLastStatus</b> method of a 
<a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the <b>FontFamily</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a> object and then checks the status of the call to create the object. If the call was successful, the example draws text.

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




<a href="https://msdn.microsoft.com/en-us/library/ms533819(v=VS.85).aspx">Constructing Font Families and Fonts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534439(v=VS.85).aspx">FontFamily</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>
 

 

