---
UID: NF:vmr9.IVMRImagePresenterConfig9.GetRenderingPrefs
title: IVMRImagePresenterConfig9::GetRenderingPrefs method
author: windows-driver-content
description: The GetRenderingPrefs method gets the current rendering preferences from the VMR-9 filter's allocator-presenter.
old-location: dshow\ivmrimagepresenterconfig9_getrenderingprefs.htm
old-project: DirectShow
ms.assetid: dfa9c81d-cfc8-401b-b4d1-50f21b528135
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRenderingPrefs method [DirectShow], GetRenderingPrefs method [DirectShow], IVMRImagePresenterConfig9 interface, GetRenderingPrefs,IVMRImagePresenterConfig9.GetRenderingPrefs, IVMRImagePresenterConfig9, IVMRImagePresenterConfig9 interface [DirectShow], GetRenderingPrefs method, IVMRImagePresenterConfig9::GetRenderingPrefs, IVMRImagePresenterConfig9GetRenderingPrefs, dshow.ivmrimagepresenterconfig9_getrenderingprefs, vmr9/IVMRImagePresenterConfig9::GetRenderingPrefs
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
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRImagePresenterConfig9.GetRenderingPrefs
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRImagePresenterConfig9::GetRenderingPrefs method


## -description



The <code>GetRenderingPrefs</code> method gets the current rendering preferences from the VMR-9 filter's allocator-presenter.



The VMR-9 filter's <a href="https://msdn.microsoft.com/b82a9dbe-aa86-4153-945b-fe8968faa5ca">IVMRFilterConfig9::GetRenderingPrefs</a> method calls through to this method.


## -parameters




### -param dwRenderFlags [out]

Receives a bitwise OR of flag from the <a href="https://msdn.microsoft.com/a32119c2-a10d-41a0-b3e9-500323eb3094">VMR9RenderPrefs</a> enumeration, indicating the current rendering settings on the allocator-presenter.


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
 

 

