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

# PFNProgressNotification callback function


## -description


Application defined callback function called when codec component progress is made.


## -parameters




### -param pvData

Type: <b>LPVOID</b>

Component data passed to the callback function.


### -param uFrameNum

Type: <b>ULONG</b>

The current frame number.


### -param operation

Type: <b><a href="https://msdn.microsoft.com/407b982d-7232-42ce-9ff5-7029b7d922a4">WICProgressOperation</a></b>

The current operation the component is in.


### -param dblProgress

Type: <b>double</b>

The progress value. The range is 0.0 to 1.0.


## -returns



Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An operation can be canceled by returning <code>WINCODEC_ERR_ABORTED</code>.

To register your callback function, query the encoder or decoder for the <a href="https://msdn.microsoft.com/8cf3fbca-0953-4dd7-aa44-3e1924cfd8b0">IWICBitmapCodecProgressNotification</a> interface and call <a href="https://msdn.microsoft.com/ac47178a-f149-4313-8673-ece59e88cfb3">RegisterProgressNotification</a>.




## -see-also




<b>Reference</b>



<a href="https://msdn.microsoft.com/6d7ef6f1-2024-4de5-9c2e-8edc6359f79b">WICProgressNotification</a>



<a href="https://msdn.microsoft.com/407b982d-7232-42ce-9ff5-7029b7d922a4">WICProgressOperation</a>
 

 

