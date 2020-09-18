---
UID: NF:mi.MI_Context_WriteProgress
title: MI_Context_WriteProgress function (mi.h)
description: Sends a progress message to the client.
helpviewer_keywords: ["MI_Context_WriteProgress","MI_Context_WriteProgress function [Windows Management Infrastructure (MI)]","mi/MI_Context_WriteProgress","wmi.mi_writeprogress","wmi_v2.mi_context_writeprogress"]
old-location: wmi_v2\mi_context_writeprogress.htm
tech.root: wmi_v2
ms.assetid: 260d46f3-b048-4278-acde-724323166ba2
ms.date: 12/05/2018
ms.keywords: MI_Context_WriteProgress, MI_Context_WriteProgress function [Windows Management Infrastructure (MI)], mi/MI_Context_WriteProgress, wmi.mi_writeprogress, wmi_v2.mi_context_writeprogress
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,     Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Context_WriteProgress
 - mi/MI_Context_WriteProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Context_WriteProgress
---

# MI_Context_WriteProgress function


## -description

Sends a progress message to the client.

## -parameters

### -param context [in]

Request context.

### -param activity [in]

A null-terminated string that represents the current activity. This string should be localized based on the 
      client UI request (retrieved through the 
      <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocale">MI_Context_GetLocale</a> function).

### -param currentOperation [in]

A null-terminated string that represents the current operation being processed. This string should be 
      localized based on the client UI request.

### -param statusDescription [in]

A null-terminated string that represents the current status description. This string should be localized 
      based on the client UI request.

### -param percentComplete

Current percentage of completion. Passing 0xffffffff indicates that the percentage complete is 
      unknown.

### -param secondsRemaining

Estimated seconds remaining to complete the current operation. Passing 0xffffffff indicates that the time 
      required to complete the current operation is unknown.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.

## -remarks

A provider calls this function to indicate how far through an operation the provider is and how much time is 
    remaining. A client can optionally register to receive these messages via an asynchronous callback. If a client 
    does not register for these messages, the server will ignore the message. This function is particularly important 
    for long running operations so the client does not think the operation has stopped responding. Do not send too 
    many progress messages as it can cause a performance hit, but send them often enough that the client does not 
    think the operation has stopped responding and possibly cancel the operation. (An interval range between 0.5 and 
    10 seconds is probably reasonable.) Also, if a progress message comes in during an operation, it will reset the 
    operation timeout period to allow the operation to last longer than the operation timeout value. If the client 
    does not register for this callback, though, it has no way of resetting the timeout value, so it may time out even 
    when the provider sends a progress message.

## -see-also

<a href="/windows/desktop/api/mi/ns-mi-mi_context">MI_Context</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_getlocale">MI_Context_GetLocale</a>