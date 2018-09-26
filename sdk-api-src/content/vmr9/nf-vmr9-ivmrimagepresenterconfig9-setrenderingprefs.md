---
UID: NF:vmr9.IVMRImagePresenterConfig9.SetRenderingPrefs
title: IVMRImagePresenterConfig9::SetRenderingPrefs
author: windows-sdk-content
description: The SetRenderingPrefs method sets the rendering preferences on the VMR-9 filter's allocator-presenter.
old-location: dshow\ivmrimagepresenterconfig9_setrenderingprefs.htm
tech.root: DirectShow
ms.assetid: 53ca84c5-6f6e-403f-baff-6b2ce66c2ce9
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IVMRImagePresenterConfig9 interface [DirectShow],SetRenderingPrefs method, IVMRImagePresenterConfig9.SetRenderingPrefs, IVMRImagePresenterConfig9::SetRenderingPrefs, IVMRImagePresenterConfig9SetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [DirectShow], SetRenderingPrefs method [DirectShow],IVMRImagePresenterConfig9 interface, dshow.ivmrimagepresenterconfig9_setrenderingprefs, vmr9/IVMRImagePresenterConfig9::SetRenderingPrefs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRImagePresenterConfig9.SetRenderingPrefs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

