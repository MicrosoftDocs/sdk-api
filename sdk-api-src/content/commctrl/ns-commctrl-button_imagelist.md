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

# BUTTON_IMAGELIST structure


## -description


Contains information about an image list that is used with a button control.


## -struct-fields




### -field himl

Type: <b>HIMAGELIST</b>

A handle to the image list. The provider retains ownership of the image list and is ultimately responsible for its disposal. Under Windows Vista, you can pass BCCL_NOGLYPH in this parameter to indicate that no glyph should be displayed.


### -field margin

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> that specifies the margin around the icon.


### -field uAlign

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A <b>UINT</b> that specifies the alignment to use. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_LEFT"></a><a id="button_imagelist_align_left"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the left margin.

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_RIGHT"></a><a id="button_imagelist_align_right"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the right margin.

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_TOP"></a><a id="button_imagelist_align_top"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_TOP</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the top margin

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_BOTTOM"></a><a id="button_imagelist_align_bottom"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Align the image with the bottom margin

</td>
</tr>
<tr>
<td width="40%"><a id="BUTTON_IMAGELIST_ALIGN_CENTER"></a><a id="button_imagelist_align_center"></a><dl>
<dt><b>BUTTON_IMAGELIST_ALIGN_CENTER</b></dt>
</dl>
</td>
<td width="60%">
Center the image.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/79383758-53d4-4955-b472-befd338cbec6">BCM_GETIMAGELIST</a>



<a href="https://msdn.microsoft.com/805d2d9b-3e8f-4323-abaf-0dd5765cd740">BCM_SETIMAGELIST</a>



<a href="https://msdn.microsoft.com/e194640a-92b7-4ba5-b80c-51a1da9c32cf">Button_GetImageList</a>



<a href="https://msdn.microsoft.com/37d449aa-a503-4ca4-98dc-dae9a1838228">Button_SetImageList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545234">Buttons</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

