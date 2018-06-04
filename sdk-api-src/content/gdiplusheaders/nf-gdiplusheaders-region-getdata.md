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
					<a href="https://msdn.microsoft.com/748cbc1c-cf0c-461f-ac14-52cf882a33b4">Region::GetDataSize</a> method. 


### -param sizeFilled [out]

Type: <b>UINT*</b>

Optional. Pointer to an 
					<b>INT</b> that receives the number of bytes of data actually received by the 
					<i>buffer</i> array. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



The 
				<a href="https://msdn.microsoft.com/748cbc1c-cf0c-461f-ac14-52cf882a33b4">Region::GetDataSize</a> method can be used before the <b>Region::GetData</b> method to determine the number of bytes needed to store the region data. Then, you can allocate a buffer that is the correct size to store the region data and set the 
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


