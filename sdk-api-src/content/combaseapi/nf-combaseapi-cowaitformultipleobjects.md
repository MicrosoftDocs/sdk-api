---
UID: NF:combaseapi.CoWaitForMultipleObjects
title: CoWaitForMultipleObjects function (combaseapi.h)
description: A replacement for CoWaitForMultipleHandles. This replacement API hides the options for CoWaitForMultipleHandles that are not supported in ASTA.
helpviewer_keywords: ["CoWaitForMultipleObjects","CoWaitForMultipleObjects function [COM]","com.cowaitformultipleobjects","combaseapi/CoWaitForMultipleObjects"]
old-location: com\cowaitformultipleobjects.htm
tech.root: com
ms.assetid: 7A14E4F4-20F0-43FF-8D64-9AAC34B8D56F
ms.date: 12/05/2018
ms.keywords: CoWaitForMultipleObjects, CoWaitForMultipleObjects function [COM], com.cowaitformultipleobjects, combaseapi/CoWaitForMultipleObjects
req.header: combaseapi.h
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
req.dll: Combase.dll; Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoWaitForMultipleObjects
 - combaseapi/CoWaitForMultipleObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - combase.dll
 - ole32.dll
 - API-MS-Win-Core-COM-l1-1-0.dll
 - API-MS-Win-Core-COM-l1-1-1.dll
api_name:
 - CoWaitForMultipleObjects
---

# CoWaitForMultipleObjects function


## -description

A replacement for <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a>. This replacement API hides the options for <b>CoWaitForMultipleHandles</b> that are not supported in ASTA.

## -parameters

### -param dwFlags [in]

<a href="/windows/desktop/api/combaseapi/ne-combaseapi-cwmo_flags">CWMO_FLAGS</a> flag controlling whether call/window message reentrancy is enabled from this wait. By default, neither COM calls nor window messages are dispatched from <b>CoWaitForMultipleObjects</b> in ASTA.

### -param dwTimeout [in]

The timeout in milliseconds of the wait.

### -param cHandles [in]

The length of the <i>pHandles</i> array. Must be &lt;= 56.

### -param pHandles [in]

An array of handles to waitable kernel objects.

### -param lpdwindex [out]

Receives the index of the handle that satisfied the wait.

## -returns

Same return values as <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a>, except the ASTA-specific CO_E_NOTSUPPORTED cases instead return E_INVALIDARG from all apartment types.