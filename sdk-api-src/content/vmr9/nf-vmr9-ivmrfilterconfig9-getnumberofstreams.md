---
UID: NF:vmr9.IVMRFilterConfig9.GetNumberOfStreams
title: IVMRFilterConfig9::GetNumberOfStreams
author: windows-sdk-content
description: The GetNumberOfStreams method retrieves the number of input streams being mixed.
old-location: dshow\ivmrfilterconfig9_getnumberofstreams.htm
tech.root: DirectShow
ms.assetid: 34b26c3a-ac5d-479e-ac9d-c782cd5dded8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetNumberOfStreams, GetNumberOfStreams method [DirectShow], GetNumberOfStreams method [DirectShow],IVMRFilterConfig9 interface, IVMRFilterConfig9 interface [DirectShow],GetNumberOfStreams method, IVMRFilterConfig9.GetNumberOfStreams, IVMRFilterConfig9::GetNumberOfStreams, IVMRFilterConfig9GetNumberOfStreams, dshow.ivmrfilterconfig9_getnumberofstreams, vmr9/IVMRFilterConfig9::GetNumberOfStreams
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
 - IVMRFilterConfig9.GetNumberOfStreams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRFilterConfig9::GetNumberOfStreams


## -description



The <code>GetNumberOfStreams</code> method retrieves the number of input streams being mixed.




## -parameters




### -param pdwMaxStreams [out]

Receives the number of streams being mixed, which is equal to the number of input pins on the VMR.


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
<i>PdwMaxStreams</i> is invalid

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/089e44c8-6a27-410d-aad5-08816bd4f915">IVMRFilterConfig9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

