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

# Region::GetDataSize


## -description


The <b>Region::GetDataSize</b> method gets the number of bytes of data that describes this region.


## -parameters






## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns the number of bytes of region data.




## -remarks



The <b>Region::GetDataSize</b> method can be used before the <a href="https://msdn.microsoft.com/36f30045-1307-4477-83e3-546c536a7f5e">Region::GetData</a> method to determine the number of bytes needed to store the region data. Then, you can allocate a buffer that is the correct size to store the region data that is obtained by the <b>Region::GetData</b>.


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
   Region pathRegion(&amp;path); 

   // Get the region data.
   UINT bufferSize = 0;
   UINT sizeFilled = 0;
   BYTE* pData = NULL;

   bufferSize = pathRegion.GetDataSize();
   pData = (BYTE*)malloc(bufferSize*sizeof(BYTE));
   pathRegion.GetData(pData, bufferSize, &amp;sizeFilled);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>



<a href="https://msdn.microsoft.com/36f30045-1307-4477-83e3-546c536a7f5e">Region::GetData</a>
 

 

