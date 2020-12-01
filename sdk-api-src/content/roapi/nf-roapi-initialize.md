---
UID: NF:roapi.Initialize
title: Initialize function (roapi.h)
description: Initializes a thread to use Windows Runtime APIs.
helpviewer_keywords: ["Initialize","Initialize function [COM]","com.initialize","roapi/Initialize"]
old-location: com\initialize.htm
tech.root: com
ms.assetid: 615E552B-46EF-4D94-BF60-A44885731F75
ms.date: 12/05/2018
ms.keywords: Initialize, Initialize function [COM], com.initialize, roapi/Initialize
req.header: roapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Initialize
 - roapi/Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ROApi.h
api_name:
 - Initialize
---

# Initialize function


## -description

Initializes a thread to use Windows Runtime APIs.

## -parameters

### -param initType

Specifies the apartment type of the thread to be initialized.

## -returns

<ul>
<li><b>S_OK</b> - Successfully initialized for the first time on the current thread</li>
<li><b>S_FALSE</b> - Successful nested initialization (current thread was already 
        initialized for the specified apartment type)</li>
<li><b>E_INVALIDARG</b> - Invalid <i>initType</i> value</li>
<li><b>CO_E_INIT_TLS</b> - Failed to allocate COM's internal TLS structure</li>
<li><b>E_OUTOFMEMORY</b> - Failed to allocate per-thread/per-apartment structures other 
        than the TLS</li>
<li><b>RPC_E_CHANGED_MODE</b> - The current thread is already initialized for a different 
        apartment type from what is specified.</li>
</ul>

## -remarks

<b>Windows::Foundation::Initialize</b> is changed to create 
    ASTAs instead of classic STAs for the <a href="/windows/desktop/api/roapi/ne-roapi-ro_init_type">RO_INIT_TYPE</a> 
    value <b>RO_INIT_SINGLETHREADED</b>. 
    <b>Windows::Foundation::Initialize</b>(<b>RO_INIT_SINGLETHREADED</b>) 
    is not supported for desktop applications and will return <b>CO_E_NOTSUPPORTED</b> if called 
    from a process other than a Windows Store app.

For Microsoft DirectX applications, you must initialize the initial thread by using 
    <b>Windows::Foundation::Initialize</b>(<b>RO_INIT_MULTITHREADED</b>).

For an out-of-process EXE server,  you must initialize the initial thread of the server by using 
    <b>Windows::Foundation::Initialize</b>(<b>RO_INIT_MULTITHREADED</b>).

## -see-also

<a href="/windows/desktop/api/roapi/ne-roapi-ro_init_type">RO_INIT_TYPE</a>