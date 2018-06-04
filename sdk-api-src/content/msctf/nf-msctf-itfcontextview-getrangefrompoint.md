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

# ITfContextView::GetRangeFromPoint


## -description


The <b>ITfContextView::GetRangeFromPoint</b> method converts a point, in screen coordinates, to an empty range of text positioned at a corresponding location.


## -parameters




### -param ec [in]

Specifies the edit cookie with read-only access.


### -param ppt [in]

Specifies the point in screen coordinates.


### -param dwFlags [in]

Specifies the range position to return based upon the screen coordinates of the point to a character bounding box. By default, the range position returned is the character bounding box containing the screen coordinates of the point. If the point is outside a character bounding box, the method returns <b>NULL</b> or <a href="https://msdn.microsoft.com/12178252-c246-4fa4-bf7b-2445b859ec01">TF_E_INVALIDPOINT</a>. Other bit flags for this parameter are as follows.

The bit flags can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GXFPF_ROUND_NEAREST"></a><a id="gxfpf_round_nearest"></a><dl>
<dt><b>GXFPF_ROUND_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are contained in a character bounding box, the range position returned is the bounding edge closest to the screen coordinates of the point.

</td>
</tr>
<tr>
<td width="40%"><a id="GXFPF_NEAREST"></a><a id="gxfpf_nearest"></a><dl>
<dt><b>GXFPF_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are not contained in a character bounding box, the closest range position is returned.

</td>
</tr>
</table>
 


### -param ppRange [out]

Receives a pointer to the ITfRange interface.


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
<dt><b>TF_E_INVALIDPOINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>pptScreen</i> parameter does not cover any document text.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The specified edit cookie is invalid.

</td>
</tr>
</table>
 




## -remarks



<img alt="Point 1 is in character bounding box and point 2 is outside the character bounding box." border="border" src="images/RngFig01.gif"/>
By default, the method will return a range positioned at 0 for point 1 and TF_E_INVALIDPOINT for point 2. If the <i>dwFlags</i> parameter is set to <a href="https://msdn.microsoft.com/e69e5a4c-65e6-4d9b-8cb0-962524aa5d39">GXFPF_ROUND_NEAREST</a>, the method returns range position 1 for point 1. If the <i>dwFlags</i> parameter is set to GXFPF_NEAREST then the method returns range position 2 for point 2.




## -see-also




<a href="https://msdn.microsoft.com/e69e5a4c-65e6-4d9b-8cb0-962524aa5d39">GXFPF_NEAREST
      </a>



GXFPF_ROUND_NEAREST



<a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView</a>



<a href="https://msdn.microsoft.com/12178252-c246-4fa4-bf7b-2445b859ec01">TF_E_INVALIDPOINT</a>
 

 

