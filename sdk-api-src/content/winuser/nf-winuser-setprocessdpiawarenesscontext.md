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

# SetProcessDpiAwarenessContext function


## -description


It is recommended that you set the process-default DPI awareness via application manifest. See <a href="hidpi.setting_the_default_dpi_awareness_for_a_process">Setting the default DPI awareness for a process</a> for more information. Setting the process-default DPI awareness via API call can lead to unexpected application behavior.

Sets the current process to a specified dots per inch (dpi) awareness context. The DPI awareness contexts are from the <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> value.


## -parameters




### -param value [in]

A <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> handle to set.


## -returns



This function returns TRUE if the operation was successful, and FALSE otherwise. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Possible errors are <b>ERROR_INVALID_PARAMETER</b> for an invalid input, and <b>ERROR_ACCESS_DENIED</b> if the default API awareness mode for the process has already been set (via a previous API call or within the application manifest).




## -remarks



This API is a more advanced version of the previously existing <a href="https://msdn.microsoft.com/BFD64207-D35D-4258-982C-20D6FE2B46F9">SetProcessDpiAwareness</a> API, allowing for the process default to be set to the finer-grained <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> values. Most importantly, this allows you to programmatically set <b>Per Monitor v2</b> as the process default value, which is not possible with the previous API.

This method sets the default <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> for all threads within an application. Individual threads can have their DPI awareness changed from the default with the <a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a> method.

<div class="alert"><b>Important</b>  <p class="note">In general, it is recommended to not use <b>SetProcessDpiAwarenessContext</b> to set the DPI awareness for your application. If possible, you should declare the DPI awareness for your application in the application manifest. For more information, see <a href="hidpi.setting_the_default_dpi_awareness_for_a_process">Setting the default DPI awareness for a process</a>.

</div>
<div> </div>
You must call this API before you call any APIs that depend on the DPI awareness (including before creating any UI in your process). Once API awareness is set for an app, any future calls to this API will fail. This is true regardless of whether you set the DPI awareness in the manifest or by using this API.

If the DPI awareness level is not set, the default value is <b>DPI_AWARENESS_CONTEXT_UNAWARE</b>.




## -see-also




<a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a>



<a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a>



<a href="hidpi.setting_the_default_dpi_awareness_for_a_process">Setting the default DPI awareness for a process</a>
 

 

