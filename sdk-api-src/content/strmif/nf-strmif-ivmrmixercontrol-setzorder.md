---
UID: NF:strmif.IVMRMixerControl.SetZOrder
title: IVMRMixerControl::SetZOrder
author: windows-sdk-content
description: The SetZOrder method sets this video stream's position in the Z-order; larger values are further away.
old-location: dshow\ivmrmixercontrol_setzorder.htm
old-project: DirectShow
ms.assetid: f1ef562e-049c-4edf-a83c-76675e2113c6
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVMRMixerControl interface [DirectShow],SetZOrder method, IVMRMixerControl.SetZOrder, IVMRMixerControl::SetZOrder, IVMRMixerControlSetZOrder, SetZOrder, SetZOrder method [DirectShow], SetZOrder method [DirectShow],IVMRMixerControl interface, dshow.ivmrmixercontrol_setzorder, strmif/IVMRMixerControl::SetZOrder
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
-	IVMRMixerControl.SetZOrder
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRMixerControl::SetZOrder


## -description



The <code>SetZOrder</code> method sets this video stream's position in the Z-order; larger values are further away.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param dwZ






#### - dwZOrder [in]

Double word containing the stream's position within the Z-order.


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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
</table>
 




## -remarks



The default Z-order is the order in which the pins were created. You only need to use this method if you wish to modify the default Z-order.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2aefaebc-14e7-4918-9256-c5e9e3449095">IVMRMixerControl Interface</a>



<a href="https://msdn.microsoft.com/76f84c77-e528-4059-8f40-5e49db9ec567">IVMRMixerControl::GetZOrder</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

