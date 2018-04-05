---
UID: NE:d2d1_1.D2D1_DEVICE_CONTEXT_OPTIONS
title: D2D1_DEVICE_CONTEXT_OPTIONS
author: windows-driver-content
description: This specifies options that apply to the device context for its lifetime.
old-location: direct2d\__d2d1_device_context_options.htm
old-project: Direct2D
ms.assetid: be4e6eb7-0767-4faf-9f27-eeb3bed48244
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D2D1_DEVICE_CONTEXT_OPTIONS, D2D1_DEVICE_CONTEXT_OPTIONS enumeration [Direct2D], D2D1_DEVICE_CONTEXT_OPTIONS_ENABLE_MULTITHREADED_OPTIMIZATIONS, D2D1_DEVICE_CONTEXT_OPTIONS_NONE, d2d1_1/D2D1_DEVICE_CONTEXT_OPTIONS, d2d1_1/D2D1_DEVICE_CONTEXT_OPTIONS_ENABLE_MULTITHREADED_OPTIMIZATIONS, d2d1_1/D2D1_DEVICE_CONTEXT_OPTIONS_NONE, direct2d.__d2d1_device_context_options
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_DEVICE_CONTEXT_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D2d1_1.h
api_name:
-	D2D1_DEVICE_CONTEXT_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_DEVICE_CONTEXT_OPTIONS enumeration


## -description


This specifies options that apply to the device context for its lifetime.


## -enum-fields




### -field D2D1_DEVICE_CONTEXT_OPTIONS_NONE

The device context is created with default options.


### -field D2D1_DEVICE_CONTEXT_OPTIONS_ENABLE_MULTITHREADED_OPTIMIZATIONS

Distribute rendering work across multiple threads. Refer to <a href="http://msdn.microsoft.com/en-us/library/windows/desktop/dd372260(v=vs.85).aspx">Improving the performance of Direct2D apps</a> for additional notes on the use of this flag.


### -field D2D1_DEVICE_CONTEXT_OPTIONS_FORCE_DWORD



