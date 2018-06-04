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

# SHGetInverseCMAP function


## -description


<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Retrieves the inverse color table mapping for the halftone palette.


## -parameters




### -param pbMap [out]

Type: <b>BYTE*</b>

A pointer to an array of <b>BYTE</b><b>s</b> that receives the inverse color table mapping, or a pointer to an <b>LPBYTE</b> which receives a pointer to a cached copy of the inverse color table mapping, depending on the value of the <i>cbMap</i> parameter.


### -param cbMap [in]

Type: <b>ULONG</b>

The size of the buffer pointed to by <i>pbMap</i>, which also defines its contents. Two values are recognized.



#### (sizeof(BYTE*))

The buffer pointed to by <i>pbMap</i> receives a pointer to a cached copy of the inverse color map table.



#### (32768)

The buffer pointed to by <i>pbMap</i> receives a copy of the inverse color map table. The buffer must be exactly 32,768 bytes in size.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The inverse color mapping table is a table of 32,768 bytes. It contains the indexes of colors in the halftone palette. Each index is stored at a position in the buffer that corresponds to a particular RGB value expressed in 555 format. These pairings allow you to find a color in the halftone palette which is a close approximation of the original color.
                
                

For example, the method for determining a color in the halftone palette that is a close approximation for the color #306040 is as follows:

<ol>
<li>Decompose the color into its red, green, and blue components. In this case, the red component is 0x30, the green component is 0x60 and the blue component is 0x40.</li>
<li>Reassemble the color into 555 format. The formula for reducing a 24-bit RGB color into 555 format is shown here.

                        <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>((red / 8) &lt;&lt; 10) + ((blue / 8) &lt;&lt; 5) + (green / 8)</pre>
</td>
</tr>
</table></span></div>
In this example, the value in 555 format is ((0x30 / 8) &lt;&lt; 10) + ((0x60 / 8) &lt;&lt; 5) + (0x40 / 8) = 6536.

</li>
<li>The index value stored in position 6536 in the inverse color map table is the index of the color in the halftone palette that is a reasonable approximation to the color #306040.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/ba9dfa0c-98df-4922-acba-d00e9b4b0fb0">CreateHalftonePalette</a>



<a href="https://msdn.microsoft.com/89e4e19b-47be-442e-8eb4-c867bb78f36a">GetNearestColor</a>
 

 

