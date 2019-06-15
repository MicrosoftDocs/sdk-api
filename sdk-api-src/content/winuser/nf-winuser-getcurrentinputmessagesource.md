---
UID: NF:winuser.GetCurrentInputMessageSource
title: GetCurrentInputMessageSource function (winuser.h)
author: windows-sdk-content
description: Retrieves the source of the input message.
old-location: input_sourceid\getcurrentinputmessagesource.htm
tech.root: Input_SourceId
ms.assetid: 35e4ebf5-df9d-4168-9996-355204c2ab93
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentInputMessageSource, GetCurrentInputMessageSource function, input_sourceid.getcurrentinputmessagesource, inputsourceid.getcurrentinputmessagesource, winuser/GetCurrentInputMessageSource
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
ms.custom: 19H1
---

# GetCurrentInputMessageSource function


## -description


Retrieves the source of the input message.


## -parameters




### -param inputMessageSource [out]

The <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-taginput_message_source">INPUT_MESSAGE_SOURCE</a> structure that holds the device type and the ID of the input message source.

<div class="alert"><b>Note</b>  <b>deviceType</b> in <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-taginput_message_source">INPUT_MESSAGE_SOURCE</a> is set to   <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ne-winuser-taginput_message_device_type">IMDT_UNAVAILABLE</a> when <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> is used to inject input (system generated or through messages such as <a href="https://docs.microsoft.com/windows/desktop/gdi/wm-paint">WM_PAINT</a>). This remains true until  <b>SendMessage</b> returns.</div>
<div> </div>

## -returns



If this function succeeds, it returns TRUE. Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_sourceid/input-source-identification-reference">Input Source Identification Reference</a>
 

 

