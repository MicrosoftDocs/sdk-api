---
UID: NE:tdh._TDH_CONTEXT_TYPE
title: TDH_CONTEXT_TYPE (tdh.h)
description: Defines the context type.
helpviewer_keywords: ["TDH_CONTEXT_MAXIMUM","TDH_CONTEXT_PDB_PATH","TDH_CONTEXT_POINTERSIZE","TDH_CONTEXT_TYPE","TDH_CONTEXT_TYPE enumeration [ETW]","TDH_CONTEXT_WPP_GMT","TDH_CONTEXT_WPP_TMFFILE","TDH_CONTEXT_WPP_TMFSEARCHPATH","etw.tdh_context_type_enum","tdh.tdh_context_type_enum","tdh/TDH_CONTEXT_MAXIMUM","tdh/TDH_CONTEXT_PDB_PATH","tdh/TDH_CONTEXT_POINTERSIZE","tdh/TDH_CONTEXT_TYPE","tdh/TDH_CONTEXT_WPP_GMT","tdh/TDH_CONTEXT_WPP_TMFFILE","tdh/TDH_CONTEXT_WPP_TMFSEARCHPATH"]
old-location: etw\tdh_context_type_enum.htm
tech.root: ETW
ms.assetid: 7892f0d2-84f6-4543-b94e-8501e3911266
ms.date: 12/05/2018
ms.keywords: TDH_CONTEXT_MAXIMUM, TDH_CONTEXT_PDB_PATH, TDH_CONTEXT_POINTERSIZE, TDH_CONTEXT_TYPE, TDH_CONTEXT_TYPE enumeration [ETW], TDH_CONTEXT_WPP_GMT, TDH_CONTEXT_WPP_TMFFILE, TDH_CONTEXT_WPP_TMFSEARCHPATH, etw.tdh_context_type_enum, tdh.tdh_context_type_enum, tdh/TDH_CONTEXT_MAXIMUM, tdh/TDH_CONTEXT_PDB_PATH, tdh/TDH_CONTEXT_POINTERSIZE, tdh/TDH_CONTEXT_TYPE, tdh/TDH_CONTEXT_WPP_GMT, tdh/TDH_CONTEXT_WPP_TMFFILE, tdh/TDH_CONTEXT_WPP_TMFSEARCHPATH
req.header: tdh.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TDH_CONTEXT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TDH_CONTEXT_TYPE
 - tdh/_TDH_CONTEXT_TYPE
 - TDH_CONTEXT_TYPE
 - tdh/TDH_CONTEXT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - TDH_CONTEXT_TYPE
---

# TDH_CONTEXT_TYPE enumeration


## -description

Defines the context type.

## -enum-fields

### -field TDH_CONTEXT_WPP_TMFFILE

Null-terminated Unicode string that contains the name of the .tmf file used for parsing the WPP log. Typically, the .tmf file name is picked up from the event GUID so you do not have to specify the file name.

### -field TDH_CONTEXT_WPP_TMFSEARCHPATH

Null-terminated Unicode string that contains the path to the .tmf file. You do not have to specify this path if the search path contains the file. Only specify this context information if you also specify the TDH_CONTEXT_WPP_TMFFILE context type. If the file is not found, TDH searches the following locations in the given order:

<ul>
<li>The path specified in the TRACE_FORMAT_SEARCH_PATH environment variable</li>
<li>The current folder</li>
</ul>

### -field TDH_CONTEXT_WPP_GMT

A 1-byte Boolean flag that indicates if the WPP event time stamp should be converted to Universal Time Coordinate (UTC). If 1, the time stamp is converted to UTC. If 0, the time stamp is in local time. By default, the time stamp is in local time.

### -field TDH_CONTEXT_POINTERSIZE

Size, in bytes, of the pointer data types or size_t data types used in the event. Indicates if the event used 4-byte or 8-byte values. By default, the pointer size is the pointer size of the decoding computer.

To determine the size of the pointer or size_t value, use the <b>PointerSize</b> member of  <a href="/windows/desktop/ETW/trace-logfile-header">TRACE_LOGFILE_HEADER</a> (the first event you receive in your <a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> callback contains this header in the data section). However, this value may not be accurate. For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set <b>PointerSize</b> to 8.

### -field TDH_CONTEXT_PDB_PATH

Null-terminated Unicode string that contains the name of the .pdb file for the binary that contains WPP messages. This parameter can be used as an alternative to <b>TDH_CONTEXT_WPP_TMFFILE</b> or <b>TDH_CONTEXT_WPP_TMFSEARCHPATH</b>.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field TDH_CONTEXT_MAXIMUM

Reserved.

## -remarks

If you are specifying context information for a legacy ETW event, you only need to specify the TDH_CONTEXT_POINTERSIZE type—the other types are used for WPP events and are ignored for legacy ETW events.

## -see-also
<a href="/windows/desktop/api/tdh/ns-tdh-tdh_context">TDH_CONTEXT</a>