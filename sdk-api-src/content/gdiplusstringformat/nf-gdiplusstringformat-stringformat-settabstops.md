---
UID: NF:gdiplusstringformat.StringFormat.SetTabStops
title: StringFormat::SetTabStops
author: windows-sdk-content
description: The StringFormat::SetTabStops method sets the offsets for tab stops in this StringFormat object.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\settabstops.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SetTabStops, SetTabStops method [GDI+], SetTabStops method [GDI+],StringFormat class, StringFormat class [GDI+],SetTabStops method, StringFormat.SetTabStops, StringFormat::SetTabStops, _gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_, gdiplus._gdiplus_CLASS_StringFormat_SetTabStops_firstTabOffset_count_tabStops_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusstringformat.h
req.include-header: Gdiplus.h
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
 - StringFormat.SetTabStops
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# StringFormat::SetTabStops


## -description


The <b>StringFormat::SetTabStops</b> method sets the offsets for tab stops in this 
			<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object.


## -parameters




### -param firstTabOffset [in]

Type: <b>REAL</b>

Real number that specifies the initial offset position. This initial offset position is relative to the string's origin and the offset of the first tab stop is relative to the initial offset position. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of tab-stop offsets in the 
					<i>tabStops</i> array. 


### -param tabStops [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specify the tab-stop offsets. The offset of the first tab stop is the first value in the array, the offset of the second tab stop, the second value in the array, and so on. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



Each tab-stop offset in the 
				<i>tabStops</i> array, except the first one, is relative to the previous one. The first tab-stop offset is relative to the initial offset position specified by 
				<i>firstTabOffset</i>. For example, if the initial offset position is 8 and the first tab-stop offset is 50, then the first tab stop is at position 58. If the initial offset position is zero, then the first tab-stop offset is relative to position 0, the string origin.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object, sets tab stops, and uses the 
						<b>StringFormat</b> object to draw a string that contains tab characters (\t). The code also draws the string's layout rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetTabStops(HDC hdc)
{
   Graphics graphics(hdc);

   REAL         tabs[] = {150, 100, 100};
   FontFamily   fontFamily(L"Courier New");
   Font         font(&amp;fontFamily, 12, FontStyleRegular, UnitPoint);
   SolidBrush   solidBrush(Color(255, 0, 0, 255));

   StringFormat stringFormat;
   stringFormat.SetTabStops(0, 3, tabs);
   graphics.DrawString(
      L"Name\tTest 1\tTest 2\tTest 3", 
      25, 
      &amp;font, 
      RectF(20, 20, 500, 100), 
      &amp;stringFormat, 
      &amp;solidBrush);

   // Draw the rectangle that encloses the text.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&amp;pen, 20, 20, 500, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4014a602-88f6-4fac-b4b2-3dafdcff8f33">Formatting Text</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>



<a href="https://msdn.microsoft.com/51c80843-9435-4926-b699-1ee4e558cac0">StringFormat::GetTabStops</a>
 

 

