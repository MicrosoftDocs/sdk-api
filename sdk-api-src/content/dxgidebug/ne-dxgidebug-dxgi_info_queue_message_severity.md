---
UID: NE:dxgidebug.DXGI_INFO_QUEUE_MESSAGE_SEVERITY
title: DXGI_INFO_QUEUE_MESSAGE_SEVERITY (dxgidebug.h)
description: Values that specify debug message severity levels for an information queue.
helpviewer_keywords: ["DXGI_INFO_QUEUE_MESSAGE_SEVERITY","DXGI_INFO_QUEUE_MESSAGE_SEVERITY enumeration [DXGI]","DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION","DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR","DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO","DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE","DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING","direct3ddxgi.dxgi_info_queue_message_severity","dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY","dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION","dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR","dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO","dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE","dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING"]
old-location: direct3ddxgi\dxgi_info_queue_message_severity.htm
tech.root: direct3ddxgi
ms.assetid: 99F9DDC8-5CCF-4991-94AD-0A399932F5B3
ms.date: 12/05/2018
ms.keywords: DXGI_INFO_QUEUE_MESSAGE_SEVERITY, DXGI_INFO_QUEUE_MESSAGE_SEVERITY enumeration [DXGI], DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE, DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING, direct3ddxgi.dxgi_info_queue_message_severity, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE, dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_INFO_QUEUE_MESSAGE_SEVERITY
 - dxgidebug/DXGI_INFO_QUEUE_MESSAGE_SEVERITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGIDebug.h
api_name:
 - DXGI_INFO_QUEUE_MESSAGE_SEVERITY
---

# DXGI_INFO_QUEUE_MESSAGE_SEVERITY enumeration


## -description

Values that specify debug message severity levels for an information queue.

## -enum-fields

### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_CORRUPTION:0

Defines some type of corruption that has occurred.

### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_ERROR

Defines an error message.

### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_WARNING

Defines a warning message.

### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_INFO

Defines an information message.

### -field DXGI_INFO_QUEUE_MESSAGE_SEVERITY_MESSAGE

Defines a message other than corruption, error, warning, or information.

## -remarks

Use this enumeration when you call <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-getmessage">IDXGIInfoQueue::GetMessage</a> to retrieve a message and when you call <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-addmessage">IDXGIInfoQueue::AddMessage</a> to add a message. Also, use this enumeration with <a href="/windows/desktop/api/dxgidebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage">IDXGIInfoQueue::AddApplicationMessage</a>.



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>
