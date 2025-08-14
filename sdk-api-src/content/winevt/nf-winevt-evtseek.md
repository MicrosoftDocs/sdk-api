---
UID: NF:winevt.EvtSeek
title: EvtSeek function (winevt.h)
description: Seeks to a specific event in a query result set.
helpviewer_keywords: ["EvtSeek","EvtSeek function [EventLog]","wes.evtseek","winevt/EvtSeek"]
old-location: wes\evtseek.htm
tech.root: wes
ms.assetid: 62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c
ms.date: 12/05/2018
ms.keywords: EvtSeek, EvtSeek function [EventLog], wes.evtseek, winevt/EvtSeek
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
 - EvtSeek
 - winevt/EvtSeek
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
 - EvtSeek
---

# EvtSeek function


## -description

Seeks to a specific event in a query result set.

## -parameters

### -param ResultSet [in]

The handle to a query result set that the <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> function returns.

### -param Position [in]

The zero-based offset to an event in the result set. The flag that you specify in the <i>Flags</i> parameter indicates the beginning relative position in the result set from which to seek. For example, you can seek from the beginning of the results or from the end of the results. Set to 0 to move to the relative position specified by the flag.

### -param Bookmark [in]

A handle to a bookmark that the <a href="/windows/desktop/api/winevt/nf-winevt-evtcreatebookmark">EvtCreateBookmark</a> function returns. The bookmark identifies an event in the result set to which you want to seek. Set this parameter only if the  <i>Flags</i> parameter has the EvtSeekRelativeToBookmark  flag set.

### -param Timeout [in]

 Reserved. Must be zero.

### -param Flags [in]

One or more flags that indicate the relative position in the result set from which to seek. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_seek_flags">EVT_SEEK_FLAGS</a> enumeration.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. To get the error code, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

</td>
</tr>
</table>

## -remarks

You can use this function only on result sets from an Admin or Operational channel, or from .evtx log files.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/bookmarking-events">Bookmarking Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtnext">EvtNext</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a>