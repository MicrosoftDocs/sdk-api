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

# DAD_AutoScroll function


## -description


<p class="CCE_Message">[<b>DAD_AutoScroll</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions.]

Scrolls the window while an image is being dragged.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window being scrolled.


### -param pad [in]

Type: <b><a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a> structure.


### -param pptNow [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

A pointer to the current scroll coordinates.


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.




## -remarks



The function is successful and the window scrolls only when the <b>bFull</b> parameter of the <a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a> structure is <b>TRUE</b>. Each time this function is called, as long as <b>bFull</b> is <b>FALSE</b>, the <b>iNextSample</b> parameter is incremented by 1 and the current scroll coordinates and time are returned in the <b>AUTO_SCROLL_DATA</b> structure. When <b>iNextSample</b> is equal to NUM_POINTS, <b>bFull</b> is set to <b>TRUE</b>, the function succeeds, and the window scrolls.





## -see-also




<a href="https://msdn.microsoft.com/4229dd3b-1fc7-4cc7-bcc9-4e25bdc17c11">AUTO_SCROLL_DATA</a>
 

 

