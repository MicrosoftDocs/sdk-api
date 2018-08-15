---
UID: NF:combaseapi.CoWaitForMultipleObjects
title: CoWaitForMultipleObjects function
author: windows-sdk-content
description: A replacement for CoWaitForMultipleHandles. This replacement API hides the options for CoWaitForMultipleHandles that are not supported in ASTA.
old-location: com\cowaitformultipleobjects.htm
old-project: com
ms.assetid: 7A14E4F4-20F0-43FF-8D64-9AAC34B8D56F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CoWaitForMultipleObjects, CoWaitForMultipleObjects function [COM], com.cowaitformultipleobjects, combaseapi/CoWaitForMultipleObjects
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: combaseapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: REGCLS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - combase.dll
 - ole32.dll
 - API-MS-Win-Core-COM-l1-1-0.dll
 - API-MS-Win-Core-COM-l1-1-1.dll
api_name:
 - CoWaitForMultipleObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: Combase.dll; Ole32.dll
req.irql: 
---

# CoWaitForMultipleObjects function


## -description


A replacement for <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a>. This replacement API hides the options for <b>CoWaitForMultipleHandles</b> that are not supported in ASTA.


## -parameters




### -param dwFlags [in]


<a href="https://msdn.microsoft.com/5FE605A9-DE92-4CD9-9390-6C9F5189A7CB">CWMO_FLAGS</a> flag controlling whether call/window message reentrancy is enabled from this wait. By default, neither COM calls nor window messages are dispatched from <b>CoWaitForMultipleObjects</b> in ASTA.


### -param dwTimeout [in]

The timeout in milliseconds of the wait.


### -param cHandles [in]

The length of the <i>pHandles</i> array. Must be &lt;= 56.


### -param pHandles [in]

An array of handles to waitable kernel objects.


### -param lpdwindex [out]

Receives the index of the handle that satisfied the wait.


## -returns



Same return values as <a href="https://msdn.microsoft.com/3eeecd34-aa94-4a48-8b41-167a71b52860">CoWaitForMultipleHandles</a>, except the ASTA-specific CO_E_NOTSUPPORTED cases instead return E_INVALIDARG from all apartment types.



