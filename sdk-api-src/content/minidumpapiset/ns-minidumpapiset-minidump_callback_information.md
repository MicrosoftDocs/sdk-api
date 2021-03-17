---
UID: NS:minidumpapiset._MINIDUMP_CALLBACK_INFORMATION
title: MINIDUMP_CALLBACK_INFORMATION (minidumpapiset.h)
description: Contains a pointer to an optional callback function that can be used by the MiniDumpWriteDump function.
helpviewer_keywords: ["*PMINIDUMP_CALLBACK_INFORMATION","MINIDUMP_CALLBACK_INFORMATION","MINIDUMP_CALLBACK_INFORMATION structure","PMINIDUMP_CALLBACK_INFORMATION","PMINIDUMP_CALLBACK_INFORMATION structure pointer","_MINIDUMP_CALLBACK_INFORMATION","_win32_minidump_callback_information_str","base.minidump_callback_information_str","minidumpapiset/MINIDUMP_CALLBACK_INFORMATION","minidumpapiset/PMINIDUMP_CALLBACK_INFORMATION"]
old-location: base\minidump_callback_information_str.htm
tech.root: Debug
ms.assetid: 98caf4c3-8e6b-4f42-ae48-977a8392de1c
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_CALLBACK_INFORMATION, MINIDUMP_CALLBACK_INFORMATION, MINIDUMP_CALLBACK_INFORMATION structure, PMINIDUMP_CALLBACK_INFORMATION, PMINIDUMP_CALLBACK_INFORMATION structure pointer, _MINIDUMP_CALLBACK_INFORMATION, _win32_minidump_callback_information_str, base.minidump_callback_information_str, minidumpapiset/MINIDUMP_CALLBACK_INFORMATION, minidumpapiset/PMINIDUMP_CALLBACK_INFORMATION'
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
req.typenames: MINIDUMP_CALLBACK_INFORMATION, *PMINIDUMP_CALLBACK_INFORMATION
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_CALLBACK_INFORMATION
 - minidumpapiset/_MINIDUMP_CALLBACK_INFORMATION
 - PMINIDUMP_CALLBACK_INFORMATION
 - minidumpapiset/PMINIDUMP_CALLBACK_INFORMATION
 - MINIDUMP_CALLBACK_INFORMATION
 - minidumpapiset/MINIDUMP_CALLBACK_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_CALLBACK_INFORMATION
---

# MINIDUMP_CALLBACK_INFORMATION structure


## -description

Contains a pointer to an optional callback function that can be used by the 
<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function.

## -struct-fields

### -field CallbackRoutine

A pointer to the 
<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> callback function.

### -field CallbackParam

The application-defined data for <b>CallbackRoutine</b>.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>



<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>