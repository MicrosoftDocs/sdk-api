---
UID: NF:gdiplusheaders.Region.GetData
title: Region::GetData
author: windows-sdk-content
description: The Region::GetData method gets data that describes this region.
old-location: gdiplus\_gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\getdata.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetData, GetData method [GDI+], GetData method [GDI+],Region class, Region class [GDI+],GetData method, Region.GetData, Region::GetData, _gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_, gdiplus._gdiplus_CLASS_Region_GetData_buffer_bufferSize_sizeFilled_
ms.prod: windows
ms.technology: windows-sdk
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
 - Region.GetData
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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
					<a href="https://msdn.microsoft.com/library/ms534766(v=VS.85).aspx">Region::GetDataSize</a> method. 


### -param sizeFilled [out]

Type: <b>UINT*</b>

Optional. Pointer to an 
					<b>INT</b> that receives the number of bytes of data actually received by the 
					<i>buffer</i> array. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



The 
				<a href="https://msdn.microsoft.com/library/ms534766(v=VS.85).aspx">Region::GetDataSize</a> method can be used before the <b>Region::GetData</b> method to determine the number of bytes needed to store the region data. Then, you can allocate a buffer that is the correct size to store the region data and set the 
				<i>buffer</i> parameter to point to the buffer.


#### Examples



The following example creates a region from a path and then gets the data that describes the region.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetData(HDC)

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
   Region pathRegion(&amp;path); 
      
   // Get the region data.
   UINT bufferSize = 0;
   UINT sizeFilled = 0;
   BYTE* pData = NULL;
   
   bufferSize = pathRegion.GetDataSize();
   
   pData = new BYTE[bufferSize];
   pathRegion.GetData(pData, bufferSize, &amp;sizeFilled);
   
   // Inspect or use the region data.
   ...
   delete pData;
}</pre>
</td>
</tr>
</table></span></div>


