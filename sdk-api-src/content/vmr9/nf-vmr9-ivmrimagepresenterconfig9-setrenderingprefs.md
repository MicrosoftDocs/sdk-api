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

# IVMRImagePresenterConfig9::SetRenderingPrefs


## -description



The <code>SetRenderingPrefs</code> method sets the rendering preferences on the VMR-9 filter's allocator-presenter.



The VMR-9 filter's <a href="https://msdn.microsoft.com/ce274528-c759-4b43-80c7-0ba1e1275b7d">IVMRFilterConfig9::SetRenderingPrefs</a> method calls through to this method.


## -parameters




### -param dwRenderFlags [in]

A bitwise OR combination of <a href="https://msdn.microsoft.com/a32119c2-a10d-41a0-b3e9-500323eb3094">VMR9RenderPrefs</a> flags that will be used to configure the allocator-presenter.


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
</table>
 




## -remarks



Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/fc3c9b4d-0213-47d5-96e4-db582c80ca4e">IVMRImagePresenterConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

