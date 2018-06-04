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

# ReleaseDC function


## -description


The <b>ReleaseDC</b> function releases a device context (DC), freeing it for use by other applications. The effect of the <b>ReleaseDC</b> function depends on the type of DC. It frees only common and window DCs. It has no effect on class or private DCs.


## -parameters




### -param hWnd [in]

A handle to the window whose DC is to be released.


### -param hDC [in]

A handle to the DC to be released.


## -returns



The return value indicates whether the DC was released. If the DC was released, the return value is 1.

If the DC was not released, the return value is zero.




## -remarks



The application must call the <b>ReleaseDC</b> function for each call to the <a href="https://msdn.microsoft.com/9e6a135e-e337-4129-a3ad-faf9a8ac9b2d">GetWindowDC</a> function and for each call to the <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a> function that retrieves a common DC.

An application cannot use the <b>ReleaseDC</b> function to release a DC that was created by calling the <a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a> function; instead, it must use the <a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a> function. <b>ReleaseDC</b> must be called from the same thread that called <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/ab7d5224-62de-40a8-909f-564f61c45d01">Scaling an Image</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6fc443c8-da97-4196-a9ed-179a4e583849">CreateDC</a>



<a href="https://msdn.microsoft.com/1aa549a0-c95f-4385-a30e-8906f67e39cd">DeleteDC</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a>



<a href="https://msdn.microsoft.com/9e6a135e-e337-4129-a3ad-faf9a8ac9b2d">GetWindowDC</a>
 

 

