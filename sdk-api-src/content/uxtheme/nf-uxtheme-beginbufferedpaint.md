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

# BeginBufferedPaint function


## -description


Begins a buffered paint operation.


## -parameters




### -param hdcTarget

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

The handle of the target DC on which the buffer will be painted.


### -param prcTarget

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the area of the target DC in which to paint.


### -param dwFormat

Type: <b><a href="https://msdn.microsoft.com/9D6666C4-06F0-4DE0-95FA-A18082A04448">BP_BUFFERFORMAT</a></b>

A member of the <a href="https://msdn.microsoft.com/9D6666C4-06F0-4DE0-95FA-A18082A04448">BP_BUFFERFORMAT</a> enumeration that specifies the format of the buffer.


### -param pPaintParams [in]

Type: <b><a href="https://msdn.microsoft.com/46ebf529-530f-4ccd-a3f8-7fcc7c71fca7">BP_PAINTPARAMS</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/46ebf529-530f-4ccd-a3f8-7fcc7c71fca7">BP_PAINTPARAMS</a> structure that defines the paint operation parameters. This value can be <b>NULL</b>.


### -param phdc [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a>*</b>

When this function returns, points to the handle of the new device context.


## -returns



Type: <b>HPAINTBUFFER</b>

A handle to the buffered paint context. If this function fails, the return value is <b>NULL</b>, and <i>phdc</i> is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The returned handle is freed when <a href="https://msdn.microsoft.com/de2de3df-cd52-4095-a87e-d054d016c7cb">EndBufferedPaint</a> is called.

An application should call <a href="https://msdn.microsoft.com/e35fd59a-f493-4ac0-971a-d0746123e255">BufferedPaintInit</a> on the calling thread before calling <b>BeginBufferedPaint</b>, and <a href="https://msdn.microsoft.com/e6d3cae8-2f4a-4436-99c0-0606eccd3048">BufferedPaintUnInit</a> before the thread is terminated.  Failure to call <b>BufferedPaintInit</b> may result in degraded performance due to internal data being initialized and destroyed for each buffered paint operation.



