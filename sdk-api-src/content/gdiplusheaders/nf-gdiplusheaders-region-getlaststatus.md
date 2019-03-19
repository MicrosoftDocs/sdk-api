---
UID: NF:gdiplusheaders.Region.GetLastStatus
title: Region::GetLastStatus (gdiplusheaders.h)
author: windows-sdk-content
description: The Region::GetLastStatus method returns a value that indicates the nature of this Regionobject's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_Region_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\getlaststatus_54.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Region class, Region class [GDI+],GetLastStatus method, Region.GetLastStatus, Region::GetLastStatus, _gdiplus_CLASS_Region_GetLastStatus_, gdiplus._gdiplus_CLASS_Region_GetLastStatus_
ms.topic: method
req.header: gdiplusheaders.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Region.GetLastStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Region::GetLastStatus


## -description


The <b>Region::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

The <b>Region::GetLastStatus</b> method returns an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>object have failed since the previous call to <b>Region::GetLastStatus</b>, then <b>Region::GetLastStatus</b> returns <b>Ok</b>.

If at least one method invoked on this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>object has failed since the previous call to <b>Region::GetLastStatus</b>, then <b>Region::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>Region::GetLastStatus</b> immediately after constructing a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>object to determine whether the constructor succeeded.

The first time you call the <b>Region::GetLastStatus</b> method of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>object, it returns <b>Ok</b> if the constructor succeeded and all methods invoked so far on the 
				<b>Region</b>object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a region from a path. Next, the code calls <a href="https://msdn.microsoft.com/en-us/library/ms534776(v=VS.85).aspx">Region::GetBounds Methods</a>, followed by a call to <a href="https://msdn.microsoft.com/en-us/library/ms534766(v=VS.85).aspx">Region::GetDataSize</a>. The code then calls <b>Region::GetLastStatus</b>. If all method calls have been successful up to this point, <b>Region::GetLastStatus</b> returns <b>Ok</b>.


```cpp
VOID Example_GetLastStatus(HDC hdc)
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
   Region pathRegion(&path);    

   pathRegion.GetBounds(&rect, &graphics);
   size = pathRegion.GetDataSize();

   if(pathRegion.GetLastStatus() == Ok)
   {
       // All methods called thus far have been successful.
   }
}
```




