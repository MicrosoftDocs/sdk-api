---
UID: NF:strmif.IVMRSurface.GetSurface
title: IVMRSurface::GetSurface
author: windows-sdk-content
description: The GetSurface method retrieves the attached DirectDraw surface interface.
old-location: dshow\ivmrsurface_getsurface.htm
old-project: DirectShow
ms.assetid: 2fba7818-6395-47d3-98b3-347f1d4a7c6f
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IVMRSurface interface, IVMRSurface interface [DirectShow],GetSurface method, IVMRSurface.GetSurface, IVMRSurface::GetSurface, IVMRSurfaceGetSurface, dshow.ivmrsurface_getsurface, strmif/IVMRSurface::GetSurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRSurface.GetSurface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRSurface::GetSurface


## -description



The <code>GetSurface</code> method retrieves the attached DirectDraw surface interface.




## -parameters




### -param lplpSurface [out]

Address of a variable that receives a pointer to the <b>IDirectDrawSurface7</b> interface. The caller must release the interface.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No DirectDraw surface is attached to this sample.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8222ea5c-be77-4f33-83ff-073fb3e85e73">IVMRSurface Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

