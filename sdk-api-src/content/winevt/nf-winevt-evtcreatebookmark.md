---
UID: NF:winevt.EvtCreateBookmark
title: EvtCreateBookmark function (winevt.h)
description: Creates a bookmark that identifies an event in a channel.
helpviewer_keywords: ["EvtCreateBookmark","EvtCreateBookmark function [EventLog]","wes.evtcreatebookmark","winevt/EvtCreateBookmark"]
old-location: wes\evtcreatebookmark.htm
tech.root: wes
ms.assetid: 1020d923-090b-48fc-96c2-394db5cd241e
ms.date: 12/05/2018
ms.keywords: EvtCreateBookmark, EvtCreateBookmark function [EventLog], wes.evtcreatebookmark, winevt/EvtCreateBookmark
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
 - EvtCreateBookmark
 - winevt/EvtCreateBookmark
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
 - EvtCreateBookmark
---

# EvtCreateBookmark function


## -description

Creates a bookmark that identifies an event in a channel.

## -parameters

### -param BookmarkXml [in, optional]

 An XML string that contains the bookmark or <b>NULL</b> if creating a bookmark.

## -returns

A handle to the bookmark if the call succeeds; otherwise, <b>NULL</b>. If <b>NULL</b>, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

  To create a bookmark, set the <i>BookmarkXml</i> parameter to <b>NULL</b>. Before you exit, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtupdatebookmark">EvtUpdateBookmark</a> function to update the bookmark. Pass the bookmark handle to the <a href="/windows/desktop/api/winevt/nf-winevt-evtrender">EvtRender</a> function to render the bookmark as an XML string. You can then persist the string for use later. To begin consuming events from where you left off the last time, set  <i>BookmarkXml</i> to the XML string that you persisted. For a subscription, pass the bookmark handle to the <a href="/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a> function. For a query, pass the bookmark handle to the <a href="/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a> function to seek to a specific event in the query result.

If the query is against multiple channels, the bookmark handle will contain bookmarks for each channel. You cannot create a bookmark for a log file.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/bookmarking-events">Bookmarking Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtupdatebookmark">EvtUpdateBookmark</a>