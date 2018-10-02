---
UID: NF:winuser.GetCurrentInputMessageSource
title: GetCurrentInputMessageSource function
author: windows-sdk-content
description: Retrieves the source of the input message.
old-location: input_sourceid\getcurrentinputmessagesource.htm
tech.root: Input_SourceId
ms.assetid: 35e4ebf5-df9d-4168-9996-355204c2ab93
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCurrentInputMessageSource, GetCurrentInputMessageSource function, input_sourceid.getcurrentinputmessagesource, inputsourceid.getcurrentinputmessagesource, winuser/GetCurrentInputMessageSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-WMPointer-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - GetCurrentInputMessageSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentInputMessageSource function


## -description


Retrieves the source of the input message.


## -parameters




### -param inputMessageSource [out]

The <a href="https://msdn.microsoft.com/75437c0a-925a-44d9-9254-43095b281c21">INPUT_MESSAGE_SOURCE</a> structure that holds the device type and the ID of the input message source.

<div class="alert"><b>Note</b>  <b>deviceType</b> in <a href="https://msdn.microsoft.com/75437c0a-925a-44d9-9254-43095b281c21">INPUT_MESSAGE_SOURCE</a> is set to   <a href="https://msdn.microsoft.com/aaaa8d9b-1056-4fa3-afcf-43d2c4b41c0e">IMDT_UNAVAILABLE</a> when <a href="https://msdn.microsoft.com/c069c542-f854-41ff-a523-90f3855e2277">SendMessage</a> is used to inject input (system generated or through messages such as <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a>). This remains true until  <b>SendMessage</b> returns.</div>
<div> </div>

## -returns



If this function succeeds, it returns TRUE. Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1B1292B2-1BB6-4F75-8D82-CC0596B9D061">Input Source Identification Reference</a>
 

 

