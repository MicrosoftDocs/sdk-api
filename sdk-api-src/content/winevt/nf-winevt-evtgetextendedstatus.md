---
UID: NF:winevt.EvtGetExtendedStatus
title: EvtGetExtendedStatus function (winevt.h)
description: Gets a text message that contains the extended error information for the current error.
helpviewer_keywords: ["EvtGetExtendedStatus","EvtGetExtendedStatus function [EventLog]","wes.evtgetextendedstatus","winevt/EvtGetExtendedStatus"]
old-location: wes\evtgetextendedstatus.htm
tech.root: wes
ms.assetid: 49451981-b3de-4515-ae88-835f17a0a8f9
ms.date: 12/05/2018
ms.keywords: EvtGetExtendedStatus, EvtGetExtendedStatus function [EventLog], wes.evtgetextendedstatus, winevt/EvtGetExtendedStatus
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wevtapi.lib
req.dll: Wevtapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvtGetExtendedStatus
 - winevt/EvtGetExtendedStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-wevtapi-eventlog-l1-1-3.dll
 - Wevtapi.dll
api_name:
 - EvtGetExtendedStatus
---

# EvtGetExtendedStatus function


## -description

Gets a  text message that contains the extended error information for the  current error.

## -parameters

### -param BufferSize [in]

The size of the <i>Buffer</i> buffer, in characters.

### -param Buffer [in]

A caller-allocated string buffer that will receive the extended error information. You can set this parameter to <b>NULL</b> to determine the required buffer size.

### -param BufferUsed [out]

The size, in characters, of the caller-allocated buffer that the function used or the required buffer size if the function fails with ERROR_INSUFFICIENT_BUFFER.

## -returns

The return value is ERROR_SUCCESS if the call succeeded; otherwise, a Win32 error code.

## -remarks

You must call this function on the thread that generated the error and before calling another Windows Event Log function.

The <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> and <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> functions can provide extended error information if there is a problem with the specified XPath. For example, the error information can identify the character in the XPath where a parsing error occurred. To receive the extended error information for a malformed XPath, you cannot specify the EvtQueryTolerateQueryErrors flag when calling <b>EvtQuery</b> or <b>EvtSubscribe</b>.