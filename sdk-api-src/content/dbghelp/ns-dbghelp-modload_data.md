---
UID: NS:dbghelp._MODLOAD_DATA
title: MODLOAD_DATA (dbghelp.h)
description: Contains module data.
helpviewer_keywords: ["*PMODLOAD_DATA","DBHHEADER_CVMISC","DBHHEADER_DEBUGDIRS","MODLOAD_DATA","MODLOAD_DATA structure","PMODLOAD_DATA","PMODLOAD_DATA structure pointer","_MODLOAD_DATA","_win32_modload_data_str","base.modload_data_str","dbghelp/MODLOAD_DATA","dbghelp/PMODLOAD_DATA"]
old-location: base\modload_data_str.htm
tech.root: Debug
ms.assetid: aa9c2b18-01bf-4eaa-8283-584ca16fc98e
ms.date: 12/05/2018
ms.keywords: '*PMODLOAD_DATA, DBHHEADER_CVMISC, DBHHEADER_DEBUGDIRS, MODLOAD_DATA, MODLOAD_DATA structure, PMODLOAD_DATA, PMODLOAD_DATA structure pointer, _MODLOAD_DATA, _win32_modload_data_str, base.modload_data_str, dbghelp/MODLOAD_DATA, dbghelp/PMODLOAD_DATA'
req.header: dbghelp.h
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
req.typenames: MODLOAD_DATA, *PMODLOAD_DATA
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
f1_keywords:
 - _MODLOAD_DATA
 - dbghelp/_MODLOAD_DATA
 - PMODLOAD_DATA
 - dbghelp/PMODLOAD_DATA
 - MODLOAD_DATA
 - dbghelp/MODLOAD_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - MODLOAD_DATA
---

# MODLOAD_DATA structure


## -description

Contains module data.

## -struct-fields

### -field ssize

The size of this structure, in bytes.

### -field ssig

The type of data. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DBHHEADER_DEBUGDIRS"></a><a id="dbhheader_debugdirs"></a><dl>
<dt><b>DBHHEADER_DEBUGDIRS</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The <b>data</b> member is a buffer that contains an array of 
<a href="/windows/desktop/api/winnt/ns-winnt-image_debug_directory">IMAGE_DEBUG_DIRECTORY</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="DBHHEADER_CVMISC"></a><a id="dbhheader_cvmisc"></a><dl>
<dt><b>DBHHEADER_CVMISC</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The <b>data</b> member is a buffer that contains an array of <a href="/windows/desktop/api/dbghelp/ns-dbghelp-modload_cvmisc">MODLOAD_CVMISC</a> structures.

</td>
</tr>
</table>

### -field data

The data. The format of this data depends on the value of the <b>ssig</b> member.

### -field size

The size of the <b>data</b> buffer, in bytes.

### -field flags

This member is unused.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-image_debug_directory">IMAGE_DEBUG_DIRECTORY</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-modload_cvmisc">MODLOAD_CVMISC</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmoduleex">SymLoadModuleEx</a>