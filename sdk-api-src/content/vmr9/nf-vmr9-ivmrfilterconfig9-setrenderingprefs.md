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

# IVMRFilterConfig9::SetRenderingPrefs


## -description



The <code>SetRenderingPrefs</code> method sets various application preferences related to video rendering.




## -parameters




### -param dwRenderFlags [in]

Double word containing a bitwise OR of <a href="https://msdn.microsoft.com/a32119c2-a10d-41a0-b3e9-500323eb3094">VMR9RenderPrefs</a> values specifying the rendering preferences.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
No allocator-presenter is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwRenderFlags</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



This method calls through to the allocator-presenter's <a href="https://msdn.microsoft.com/53ca84c5-6f6e-403f-baff-6b2ce66c2ce9">IVMRImagePresenterConfig9::SetRenderingPrefs</a> method. (The default allocator-presenter exposes <b>IVMRImagePresenterConfig9</b>. Custom allocator-presenters can also expose this interface if desired.) If the VMR-9 has not yet created the default allocator-presenter, or if the application provided a custom allocator-presenter which does not support <b>IVMRImagePresenterConfig9</b>, this method returns VFW_E_WRONG_STATE. To create the default allocator-presenter, call <a href="https://msdn.microsoft.com/d7a27d7c-5cd4-4a20-ba15-7056d502e3e3">IVMRFilterConfig9::SetRenderingMode</a> with the value VMR9Mode_Windowed or VMR9Mode_Windowed.




## -see-also




<a href="https://msdn.microsoft.com/089e44c8-6a27-410d-aad5-08816bd4f915">IVMRFilterConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

