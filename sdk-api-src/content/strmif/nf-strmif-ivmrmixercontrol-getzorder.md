---
UID: NF:strmif.IVMRMixerControl.GetZOrder
title: IVMRMixerControl::GetZOrder
author: windows-sdk-content
description: The GetZOrder method retrieves this video stream's position in the Z order.
old-location: dshow\ivmrmixercontrol_getzorder.htm
old-project: DirectShow
ms.assetid: 76f84c77-e528-4059-8f40-5e49db9ec567
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetZOrder, GetZOrder method [DirectShow], GetZOrder method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetZOrder method, IVMRMixerControl.GetZOrder, IVMRMixerControl::GetZOrder, IVMRMixerControlGetZOrder, dshow.ivmrmixercontrol_getzorder, strmif/IVMRMixerControl::GetZOrder
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRMixerControl.GetZOrder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerControl::GetZOrder


## -description



The <code>GetZOrder</code> method retrieves this video stream's position in the Z order.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param pZ






#### - pZOrder [out]

Pointer to a DWORD that receives the current position in the Z-order.


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
<i>pZOrder</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
</table>
 




## -remarks



The default Z-order is the order in which the pins were created.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/f1ef562e-049c-4edf-a83c-76675e2113c6">IVMRMixerControl::SetZOrder</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

