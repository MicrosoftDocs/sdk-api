---
UID: NF:gdiplusheaders.Region.GetData
title: Region::GetData (gdiplusheaders.h)
description: The Region::GetData method gets data that describes this region.
helpviewer_keywords: ["GetData","GetData method [GDI+]","GetData method [GDI+]","Region class","Region class [GDI+]","GetData method","Region.GetData","Region::GetData","_gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_","gdiplus._gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_"]
old-location: gdiplus\_gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\getdata.htm
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [GDI+], GetData method [GDI+],Region class, Region class [GDI+],GetData method, Region.GetData, Region::GetData, _gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_, gdiplus._gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_
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
 - Region::GetData
 - gdiplusheaders/Region::GetData
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
 - Region.GetData
---

# Region::GetData


## -description

The <b>Region::GetData</b> method gets data that describes this region.

## -parameters

### -param buffer [out]

Type: <b>BYTE*</b>

Pointer to an array of 
					<b>BYTE</b> values that receives the region data.

### -param bufferSize [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the 
					<i>buffer</i> array. The size of the 
					<i>buffer</i> array can be greater than or equal to the number of bytes required to store the region data. The exact number of bytes required can be determined by calling the 
					<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getdatasize">Region::GetDataSize</a> method.

### -param sizeFilled [out]

Type: <b>UINT*</b>

Optional. Pointer to an 
					<b>INT</b> that receives the number of bytes of data actually received by the 
					<i>buffer</i> array. The default value is <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The 
				<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getdatasize">Region::GetDataSize</a> method can be used before the <b>Region::GetData</b> method to determine the number of bytes needed to store the region data. Then, you can allocate a buffer that is the correct size to store the region data and set the 
				<i>buffer</i> parameter to point to the buffer.


#### Examples



The following example creates a region from a path and then gets the data that describes the region.


```cpp
VOID Example_GetData(HDC)

{
   Point points[] = {
      Point(110, 20)
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
   
   pData = new BYTE[bufferSize];
   pathRegion.GetData(pData, bufferSize, &sizeFilled);
   
   // Inspect or use the region data.
   ...
   delete pData;
}
```