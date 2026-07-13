---
UID: NF:winuser.GetCurrentInputMessageSource
title: GetCurrentInputMessageSource function (winuser.h)
description: Retrieves the source of the input message.
helpviewer_keywords: ["GetCurrentInputMessageSource","GetCurrentInputMessageSource function","input_sourceid.getcurrentinputmessagesource","inputsourceid.getcurrentinputmessagesource","winuser/GetCurrentInputMessageSource"]
old-location: input_sourceid\getcurrentinputmessagesource.htm
tech.root: controls
ms.assetid: 35e4ebf5-df9d-4168-9996-355204c2ab93
ms.date: 12/05/2018
ms.keywords: GetCurrentInputMessageSource, GetCurrentInputMessageSource function, input_sourceid.getcurrentinputmessagesource, inputsourceid.getcurrentinputmessagesource, winuser/GetCurrentInputMessageSource
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentInputMessageSource
 - winuser/GetCurrentInputMessageSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-wmpointermin-l1-1-0.dll
 - api-ms-win-rtcore-ntuser-wmpointer-l1-2-0.dll
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
req.apiset: ext-ms-win-rtcore-ntuser-wmpointer-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# GetCurrentInputMessageSource function


## -description

Retrieves the source of the input message.

## -parameters

### -param inputMessageSource [out]

The <a href="/windows/desktop/api/winuser/ns-winuser-input_message_source">INPUT_MESSAGE_SOURCE</a> structure that holds the device type and the ID of the input message source.

<div class="alert"><b>Note</b>  <b>deviceType</b> in <a href="/windows/desktop/api/winuser/ns-winuser-input_message_source">INPUT_MESSAGE_SOURCE</a> is set to   <a href="/windows/desktop/api/winuser/ne-winuser-input_message_device_type">IMDT_UNAVAILABLE</a> when <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> is used to inject input (system generated or through messages such as <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a>). This remains true until  <b>SendMessage</b> returns.</div>
<div> </div>

## -returns

If this function succeeds, it returns TRUE. Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/input_sourceid/input-source-identification-reference">Input Source Identification Reference</a>
