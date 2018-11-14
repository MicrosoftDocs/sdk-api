---
UID: NF:strmif.IVMRFilterConfig.GetNumberOfStreams
title: IVMRFilterConfig::GetNumberOfStreams
author: windows-sdk-content
description: The GetNumberOfStreams method retrieves the number of input streams being mixed.
old-location: dshow\ivmrfilterconfig_getnumberofstreams.htm
tech.root: DirectShow
ms.assetid: e031c427-23bb-4243-bb38-0837a6db8c2c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetNumberOfStreams, GetNumberOfStreams method [DirectShow], GetNumberOfStreams method [DirectShow],IVMRFilterConfig interface, IVMRFilterConfig interface [DirectShow],GetNumberOfStreams method, IVMRFilterConfig.GetNumberOfStreams, IVMRFilterConfig::GetNumberOfStreams, IVMRFilterConfigGetNumberOfStreams, dshow.ivmrfilterconfig_getnumberofstreams, strmif/IVMRFilterConfig::GetNumberOfStreams
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
 - IVMRFilterConfig.GetNumberOfStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IVMRFilterConfig.GetNumberOfStreams
: 
---

# IVMRFilterConfig::GetNumberOfStreams


## -description



The <code>GetNumberOfStreams</code> method retrieves the number of input streams being mixed.




## -parameters




### -param pdwMaxStreams [out]

Pointer to a double word that receives the number of streams being mixed, which is equal to the number of input pins on the VMR.


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
<i>pdwMaxStreams</i> is invalid

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3ea7bb41-1f5f-496f-bdf4-776ec9f28876">IVMRFilterConfig Interface</a>



<a href="https://msdn.microsoft.com/cd200b33-bb74-474a-9047-d81cb470af23">IVMRFilterConfig::SetNumberOfStreams</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

