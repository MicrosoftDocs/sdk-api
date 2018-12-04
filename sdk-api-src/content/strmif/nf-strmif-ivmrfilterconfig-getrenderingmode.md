---
UID: NF:strmif.IVMRFilterConfig.GetRenderingMode
title: IVMRFilterConfig::GetRenderingMode
author: windows-sdk-content
description: The GetRenderingMode method retrieves the rendering mode currently being used by the VMR.
old-location: dshow\ivmrfilterconfig_getrenderingmode.htm
tech.root: DirectShow
ms.assetid: 139b0326-2ab1-4fa4-91ae-9115b4368660
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetRenderingMode, GetRenderingMode method [DirectShow], GetRenderingMode method [DirectShow],IVMRFilterConfig interface, IVMRFilterConfig interface [DirectShow],GetRenderingMode method, IVMRFilterConfig.GetRenderingMode, IVMRFilterConfig::GetRenderingMode, IVMRFilterConfigGetRenderingMode, dshow.ivmrfilterconfig_getrenderingmode, strmif/IVMRFilterConfig::GetRenderingMode
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVMRFilterConfig.GetRenderingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRFilterConfig::GetRenderingMode


## -description



The <code>GetRenderingMode</code> method retrieves the rendering mode currently being used by the VMR.




## -parameters




### -param pMode [out]

Pointer to a <b>DWORD</b> that receives a <a href="https://msdn.microsoft.com/cc924b1a-561f-4d62-8cc8-03ba5e5e8d5b">VMRMode</a> value indicating the current rendering mode.


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
<i>pMode</i> is invalid

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3ea7bb41-1f5f-496f-bdf4-776ec9f28876">IVMRFilterConfig Interface</a>



<a href="https://msdn.microsoft.com/11fbc818-b0c3-4ce1-b9fe-7e4ba1f81467">IVMRFilterConfig::SetRenderingMode</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

