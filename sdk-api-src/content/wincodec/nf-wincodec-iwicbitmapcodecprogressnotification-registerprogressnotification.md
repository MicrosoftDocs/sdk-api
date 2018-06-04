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

# IWICBitmapCodecProgressNotification::RegisterProgressNotification


## -description


Registers a progress notification callback function.


## -parameters




### -param pfnProgressNotification [in]

Type: <b>PFNProgressNotification</b>

A function pointer to the application defined progress notification callback function. See <a href="https://msdn.microsoft.com/10dd9fbe-abff-4fc9-a3a5-7c01ecc10a7f">ProgressNotificationCallback</a> for the callback signature.


### -param pvData [in]

Type: <b>LPVOID</b>

A pointer to component data for the callback method.


### -param dwProgressFlags [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/407b982d-7232-42ce-9ff5-7029b7d922a4">WICProgressOperation</a> and <a href="https://msdn.microsoft.com/6d7ef6f1-2024-4de5-9c2e-8edc6359f79b">WICProgressNotification</a> flags to use for progress notification.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications can only register a single callback. Subsequent registration calls will replace the previously registered callback. To unregister a callback, pass in <b>NULL</b> or register a new callback function.


            Progress is reported in an increasing order between 0.0 and 1.0. 
            If <i>dwProgressFlags</i> includes <b>WICProgressNotificationBegin</b>, the callback is guaranteed to be called with progress 0.0.
            If <i>dwProgressFlags</i> includes <b>WICProgressNotificationEnd</b>, the callback is guaranteed to be called with progress 1.0.
         

<b>WICProgressNotificationFrequent</b> increases the frequency in which the callback is called.
            If an operation is expected to take more than 30 seconds, <b>WICProgressNotificationFrequent</b> should be added to <i>dwProgressFlags</i>.
         




## -see-also




<a href="https://msdn.microsoft.com/8cf3fbca-0953-4dd7-aa44-3e1924cfd8b0">IWICBitmapCodecProgressNotification</a>



<a href="https://msdn.microsoft.com/10dd9fbe-abff-4fc9-a3a5-7c01ecc10a7f">ProgressNotificationCallback</a>
 

 

