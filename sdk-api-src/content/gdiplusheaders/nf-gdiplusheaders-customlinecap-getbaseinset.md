---
UID: NF:gdiplusheaders.CustomLineCap.GetBaseInset
title: CustomLineCap::GetBaseInset
author: windows-sdk-content
description: The CustomLineCap::GetBaseInset method gets the distance between the base cap to the start of the line.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_GetBaseInset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\getbaseinset.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: CustomLineCap class [GDI+],GetBaseInset method, CustomLineCap.GetBaseInset, CustomLineCap::GetBaseInset, GetBaseInset, GetBaseInset method [GDI+], GetBaseInset method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_GetBaseInset_, gdiplus._gdiplus_CLASS_CustomLineCap_GetBaseInset_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CustomLineCap.GetBaseInset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CustomLineCap::GetBaseInset


## -description


The <b>CustomLineCap::GetBaseInset</b> method gets the distance between the base cap to the start of the line.


## -parameters






## -returns



Type: <strong>Type: <b>REAL</b>
</strong>

This method returns the base inset value.




## -remarks



The base inset is used to separate the base cap from the start of the line. A value of 0 makes the base cap and the line touch. A value greater than 0 inserts a space (in units) between the line cap and the start of the line.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object, gets the base inset of the cap, and then creates a second <b>CustomLineCap</b> object that uses the same base inset.


```cpp
VOID Example_GetBaseInset(HDC hdc)
{
   Graphics graphics(hdc);

   //Create a Path object.
   GraphicsPath capPath;

   //Create a CustomLineCap object, and set its base cap to LineCapRound.
   CustomLineCap custCap(NULL, &capPath, LineCapRound, 5);

   // Get the base inset of custCap.
   REAL baseInset = custCap.GetBaseInset();

   // Create a second CustomLineCap object with the same base inset as the
   // first.
   CustomLineCap insetCap(NULL, &capPath, LineCapRound, baseInset);

   // Create a Pen object and assign insetCap as the custom end cap. 
   // Then draw a line.
   Pen pen(Color(255, 0, 0, 255), 5);
   pen.SetCustomEndCap(&insetCap);
   graphics.DrawLine(&pen, Point(0, 0), Point(100, 100));
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a>
 

 

