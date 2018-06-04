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

# ITfContextOwner::GetACPFromPoint


## -description


The <b>ITfContextOwner::GetACPFromPoint</b> method converts a point in screen coordinates to an application character position.


## -parameters




### -param ptScreen [in]

Pointer to the <b>POINT</b> structure with the screen coordinates of the point.


### -param dwFlags [in]

Specifies the character position to return based upon the screen coordinates of the point relative to a character bounding box. By default, the character position returned is the character bounding box containing the screen coordinates of the point. If the point is outside a character's bounding box, the method returns <b>NULL</b> or TF_E_INVALIDPOINT.

If the GXFPF_ROUND_NEAREST flag is specified for this parameter and the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.

If the GXFPF_NEAREST flag is specified for this parameter and the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.

The bit flags can be combined.


### -param pacp [out]

Receives the character position that corresponds to the screen coordinates of the point


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>ptScreen</i> parameter is not within the bounding box of any character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout.

</td>
</tr>
</table>
 




## -remarks



<img alt="Point 1 is in character bounding box and point 2 is outside the character bounding box." border="border" src="images/ACPFig01.gif"/>
Use the illustration to determine the character position returned based on the flags used in the <i>dwFlags</i> parameter.

<b>Point 1
      </b>

<ul>
<li>Default-- <i>pacp = 0</i> --The screen coordinates of the point is inside the character bounding box of Character Position 0.</li>
<li>GXPF_ROUND_NEAREST-- <i>pacp = 1</i> --The screen coordinates of the point is closest to Range Position 1 which is the starting range position of Character Position 1.</li>
<li>GXPF_NEAREST-- <i>pacp = 0</i> --The default behavior occurs because the point lies within the character bounding box of Character Position 0.</li>
</ul>
<b>Point 2</b>

<ul>
<li>Default-- <i>hr = TF_E_INVALIDPOINT</i> --The screen coordinates of the point is outside a character bounding box.</li>
<li>GXPF_ROUND_NEAREST-- <i>hr = TF_E_INVALIDPOINT</i> --The default behavior occurs because the screen coordinates of the point is outside a character bounding box.</li>
<li>GXPF_NEAREST-- <i>pacp = 1</i> --The closest character position to the screen coordinates of the point is Character Position 1.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">
        ITextStoreACP::GetACPFromPoint
      </a>



<a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a>



<a href="https://msdn.microsoft.com/543761fe-420e-4821-a69f-abc6c853677e">ITfContextView::GetRangeFromPoint
      </a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">
        TsViewCookie
      </a>
 

 

