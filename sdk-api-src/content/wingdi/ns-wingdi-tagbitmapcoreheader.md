---
UID: NS:wingdi.tagBITMAPCOREHEADER
title: tagBITMAPCOREHEADER
author: windows-sdk-content
description: The BITMAPCOREHEADER structure contains information about the dimensions and color format of a DIB.
old-location: gdi\bitmapcoreheader.htm
old-project: gdi
ms.assetid: 0182adcd-dbba-43de-b41b-ab2f0fd8f7bf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPBITMAPCOREHEADER, *PBITMAPCOREHEADER, BITMAPCOREHEADER, BITMAPCOREHEADER structure [Windows GDI], PBITMAPCOREHEADER, PBITMAPCOREHEADER structure pointer [Windows GDI], _win32_BITMAPCOREHEADER_str, gdi.bitmapcoreheader, tagBITMAPCOREHEADER, wingdi/BITMAPCOREHEADER, wingdi/PBITMAPCOREHEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: BITMAPCOREHEADER, *LPBITMAPCOREHEADER, *PBITMAPCOREHEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - BITMAPCOREHEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagBITMAPCOREHEADER structure


## -description



The <b>BITMAPCOREHEADER</b> structure contains information about the dimensions and color format of a DIB.




## -struct-fields




### -field bcSize

The number of bytes required by the structure.


### -field bcWidth

The width of the bitmap, in pixels.


### -field bcHeight

The height of the bitmap, in pixels.


### -field bcPlanes

The number of planes for the target device. This value must be 1.


### -field bcBitCount

The number of bits-per-pixel. This value must be 1, 4, 8, or 24.


## -remarks



The <a href="https://msdn.microsoft.com/cb6cb9da-8f7f-47e9-980a-aa77fe04c80c">BITMAPCOREINFO</a> structure combines the <b>BITMAPCOREHEADER</b> structure and a color table to provide a complete definition of the dimensions and colors of a DIB. For more information about specifying a DIB, see <b>BITMAPCOREINFO</b>.

An application should use the information stored in the <b>bcSize</b> member to locate the color table in a <a href="https://msdn.microsoft.com/cb6cb9da-8f7f-47e9-980a-aa77fe04c80c">BITMAPCOREINFO</a> structure, using a method such as the following:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
pColor = ((LPBYTE) pBitmapCoreInfo + 
        (WORD) (pBitmapCoreInfo -&gt; bcSize)) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/cb6cb9da-8f7f-47e9-980a-aa77fe04c80c">BITMAPCOREINFO</a>



<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>
 

 

