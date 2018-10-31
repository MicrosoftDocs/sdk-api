---
UID: NF:vmr9.IVMRFilterConfig9.GetRenderingMode
title: IVMRFilterConfig9::GetRenderingMode
author: windows-sdk-content
description: The GetRenderingMode method retrieves the rendering mode currently being used by the VMR.
old-location: dshow\ivmrfilterconfig9_getrenderingmode.htm
tech.root: DirectShow
ms.assetid: e39077ce-737f-4dd9-ab7d-4dc087828fdf
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetRenderingMode, GetRenderingMode method [DirectShow], GetRenderingMode method [DirectShow],IVMRFilterConfig9 interface, IVMRFilterConfig9 interface [DirectShow],GetRenderingMode method, IVMRFilterConfig9.GetRenderingMode, IVMRFilterConfig9::GetRenderingMode, IVMRFilterConfig9GetRenderingMode, dshow.ivmrfilterconfig9_getrenderingmode, vmr9/IVMRFilterConfig9::GetRenderingMode
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
 - IVMRFilterConfig9.GetRenderingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRFilterConfig9::GetRenderingMode


## -description



The <code>GetRenderingMode</code> method retrieves the rendering mode currently being used by the VMR.




## -parameters




### -param pMode [out]

Receives a member of the <a href="https://msdn.microsoft.com/708c45e4-e92b-4fe5-900f-7cd806011f5e">VMR9Mode</a> emumeration.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pMode</i> is invalid

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/089e44c8-6a27-410d-aad5-08816bd4f915">IVMRFilterConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

