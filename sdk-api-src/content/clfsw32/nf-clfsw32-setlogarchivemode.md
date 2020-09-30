---
UID: NF:clfsw32.SetLogArchiveMode
title: SetLogArchiveMode function (clfsw32.h)
description: Enables or disables log archive support for a specified log.
helpviewer_keywords: ["CLFS_LOG_ARCHIVE_MODE","ClfsLogArchiveDisabled","ClfsLogArchiveEnabled","SetLogArchiveMode","SetLogArchiveMode function [Files]","clfsw32/SetLogArchiveMode","fs.setlogarchivemode"]
old-location: fs\setlogarchivemode.htm
tech.root: fs
ms.assetid: 9f8a9ab9-2873-44c2-aa8d-78514ffe42bb
ms.date: 12/05/2018
ms.keywords: CLFS_LOG_ARCHIVE_MODE, ClfsLogArchiveDisabled, ClfsLogArchiveEnabled, SetLogArchiveMode, SetLogArchiveMode function [Files], clfsw32/SetLogArchiveMode, fs.setlogarchivemode
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClfsW32.lib
req.dll: ClfsW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetLogArchiveMode
 - clfsw32/SetLogArchiveMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClfsW32.dll
api_name:
 - SetLogArchiveMode
---

# SetLogArchiveMode function


## -description

Enables or disables log archive support for a specified log.

## -parameters

### -param hLog [in]

A handle to the log that is obtained from 
      <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.

### -param eMode [in]

Specifies whether to make the log ephemeral. This parameter can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsLogArchiveEnabled"></a><a id="clfslogarchiveenabled"></a><a id="CLFSLOGARCHIVEENABLED"></a><dl>
<dt><b>ClfsLogArchiveEnabled</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Enable log archive (ephemeral logs) support.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsLogArchiveDisabled"></a><a id="clfslogarchivedisabled"></a><a id="CLFSLOGARCHIVEDISABLED"></a><dl>
<dt><b>ClfsLogArchiveDisabled</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Disables ephemeral logs.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>