---
UID: NC:minidumpapiset.MINIDUMP_CALLBACK_ROUTINE
title: MINIDUMP_CALLBACK_ROUTINE (minidumpapiset.h)
description: An application-defined callback function used with MiniDumpWriteDump. It receives extended minidump information.
helpviewer_keywords: ["MINIDUMP_CALLBACK_ROUTINE","MiniDumpCallback","MiniDumpCallback callback","MiniDumpCallback callback function","_win32_minidumpcallback","base.minidumpcallback","minidumpapiset/MiniDumpCallback"]
old-location: base\minidumpcallback.htm
tech.root: Debug
ms.assetid: 8dc95b0a-6aee-4c38-ab25-a800153bbe91
ms.date: 12/05/2018
ms.keywords: MINIDUMP_CALLBACK_ROUTINE, MiniDumpCallback, MiniDumpCallback callback, MiniDumpCallback callback function, _win32_minidumpcallback, base.minidumpcallback, minidumpapiset/MiniDumpCallback
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - MINIDUMP_CALLBACK_ROUTINE
 - minidumpapiset/MINIDUMP_CALLBACK_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - minidumpapiset.h
api_name:
 - MiniDumpCallback
---

# MINIDUMP_CALLBACK_ROUTINE callback function


## -description

An application-defined callback function used with 
<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>. It receives extended minidump information.

The <b>MINIDUMP_CALLBACK_ROUTINE</b> type defines a pointer to this callback function. 
<b>MiniDumpCallback</b> is a placeholder for the application-defined function name.

## -parameters

### -param CallbackParam [in]

An application-defined parameter value.

### -param CallbackInput [in]

A pointer to a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a> structure that specifies extended minidump information.

### -param CallbackOutput [in, out]

A pointer to a 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> structure that receives application-defined information from the callback function.

## -returns

If the function succeeds, return <b>TRUE</b>; otherwise, return <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_information">MINIDUMP_CALLBACK_INFORMATION</a>



<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>