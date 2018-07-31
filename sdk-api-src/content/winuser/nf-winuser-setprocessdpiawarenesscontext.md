---
UID: NF:winuser.SetProcessDpiAwarenessContext
title: SetProcessDpiAwarenessContext function
author: windows-sdk-content
description: Sets the current process to a specified dots per inch (dpi) awareness context. The DPI awareness contexts are from the DPI_AWARENESS_CONTEXT value.
old-location: hidpi\setprocessdpiawarenesscontext.htm
old-project: hidpi
ms.assetid: EACD1784-BEFF-46C1-8665-CBC86A65833C
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetProcessDpiAwarenessContext, SetProcessDpiAwarenessContext function [High DPI], hidpi.setprocessdpiawarenesscontext, winuser/SetProcessDpiAwarenessContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetProcessDpiAwarenessContext
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetProcessDpiAwarenessContext function


## -description


It is recommended that you set the process-default DPI awareness via application manifest. See <a href="https://msdn.microsoft.com/C9488338-D863-45DF-B5CB-7ED9B869A5E2">Setting the default DPI awareness for a process</a> for more information. Setting the process-default DPI awareness via API call can lead to unexpected application behavior.

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

<div class="alert"><b>Important</b>  <p class="note">In general, it is recommended to not use <b>SetProcessDpiAwarenessContext</b> to set the DPI awareness for your application. If possible, you should declare the DPI awareness for your application in the application manifest. For more information, see <a href="https://msdn.microsoft.com/C9488338-D863-45DF-B5CB-7ED9B869A5E2">Setting the default DPI awareness for a process</a>.

</div>
<div> </div>
You must call this API before you call any APIs that depend on the DPI awareness (including before creating any UI in your process). Once API awareness is set for an app, any future calls to this API will fail. This is true regardless of whether you set the DPI awareness in the manifest or by using this API.

If the DPI awareness level is not set, the default value is <b>DPI_AWARENESS_CONTEXT_UNAWARE</b>.




## -see-also




<a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a>



<a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a>



<a href="https://msdn.microsoft.com/C9488338-D863-45DF-B5CB-7ED9B869A5E2">Setting the default DPI awareness for a process</a>
 

 

