---
UID: NF:winevt.EvtUpdateBookmark
title: EvtUpdateBookmark function (winevt.h)
description: Updates the bookmark with information that identifies the specified event.
helpviewer_keywords: ["EvtUpdateBookmark","EvtUpdateBookmark function [EventLog]","wes.evtupdatebookmark","winevt/EvtUpdateBookmark"]
old-location: wes\evtupdatebookmark.htm
tech.root: wes
ms.assetid: aa31f0cf-b37a-40bb-922e-2b987b8a9dcf
ms.date: 12/05/2018
ms.keywords: EvtUpdateBookmark, EvtUpdateBookmark function [EventLog], wes.evtupdatebookmark, winevt/EvtUpdateBookmark
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
 - EvtUpdateBookmark
 - winevt/EvtUpdateBookmark
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
 - EvtUpdateBookmark
---

# EvtUpdateBookmark function


## -description

Updates the bookmark with information that identifies the specified event.

## -parameters

### -param Bookmark [in]

The handle to the bookmark to be updated. The <a href="/windows/desktop/api/winevt/nf-winevt-evtcreatebookmark">EvtCreateBookmark</a> function returns this handle.

### -param Event [in]

The handle to the event to bookmark.

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
The function succeeded.

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
The function failed. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtcreatebookmark">EvtCreateBookmark</a>