---
UID: NF:gdiplusheaders.Region.GetDataSize
title: Region::GetDataSize (gdiplusheaders.h)
description: The Region::GetDataSize method gets the number of bytes of data that describes this region.
helpviewer_keywords: ["GetDataSize","GetDataSize method [GDI+]","GetDataSize method [GDI+]","Region class","Region class [GDI+]","GetDataSize method","Region.GetDataSize","Region::GetDataSize","_gdiplus_CLASS_Region_GetDataSize_","gdiplus._gdiplus_CLASS_Region_GetDataSize_"]
old-location: gdiplus\_gdiplus_CLASS_Region_GetDataSize_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\getdatasize.htm
ms.date: 12/05/2018
ms.keywords: GetDataSize, GetDataSize method [GDI+], GetDataSize method [GDI+],Region class, Region class [GDI+],GetDataSize method, Region.GetDataSize, Region::GetDataSize, _gdiplus_CLASS_Region_GetDataSize_, gdiplus._gdiplus_CLASS_Region_GetDataSize_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Region::GetDataSize
 - gdiplusheaders/Region::GetDataSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Region.GetDataSize
---

# Region::GetDataSize


## -description

The <b>Region::GetDataSize</b> method gets the number of bytes of data that describes this region.



## -returns

Type: <b>UINT</b>

This method returns the number of bytes of region data.

## -remarks

The <b>Region::GetDataSize</b> method can be used before the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getdata">Region::GetData</a> method to determine the number of bytes needed to store the region data. Then, you can allocate a buffer that is the correct size to store the region data that is obtained by the <b>Region::GetData</b>.


#### Examples



The following example creates a region from a path and then gets the data that describes the region.


```cpp
VOID Example_GetData(HDC)
{
   Point points[] = 
      Point(110, 20),
      Point(120, 30),
      Point(100, 60),
      Point(120, 70),
      Point(150, 60),
      Point(140, 10)};

   GraphicsPath path;
   path.AddClosedCurve(points, 6);

   // Create a region from a path.
   Region pathRegion(&path); 

   // Get the region data.
   UINT bufferSize = 0;
   UINT sizeFilled = 0;
   BYTE* pData = NULL;

   bufferSize = pathRegion.GetDataSize();
   pData = (BYTE*)malloc(bufferSize*sizeof(BYTE));
   pathRegion.GetData(pData, bufferSize, &sizeFilled);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getdata">Region::GetData</a>
