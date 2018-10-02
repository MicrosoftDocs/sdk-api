---
UID: NF:winevt.EvtCreateBookmark
title: EvtCreateBookmark function
author: windows-sdk-content
description: Creates a bookmark that identifies an event in a channel.
old-location: wes\evtcreatebookmark.htm
tech.root: WES
ms.assetid: 1020d923-090b-48fc-96c2-394db5cd241e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EvtCreateBookmark, EvtCreateBookmark function [EventLog], wes.evtcreatebookmark, winevt/EvtCreateBookmark
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wevtapi.dll
api_name:
 - EvtCreateBookmark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtCreateBookmark function


## -description


Creates a bookmark that identifies an event in a channel.


## -parameters




### -param BookmarkXml [in, optional]

 An XML string that contains the bookmark or <b>NULL</b> if creating a bookmark.


## -returns



A handle to the bookmark if the call succeeds; otherwise, <b>NULL</b>. If <b>NULL</b>, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



  To create a bookmark, set the <i>BookmarkXml</i> parameter to <b>NULL</b>. Before you exit, call the <a href="https://msdn.microsoft.com/aa31f0cf-b37a-40bb-922e-2b987b8a9dcf">EvtUpdateBookmark</a> function to update the bookmark. Pass the bookmark handle to the <a href="https://msdn.microsoft.com/521322b6-3424-4321-bcba-fa8dcdc05a76">EvtRender</a> function to render the bookmark as an XML string. You can then persist the string for use later. To begin consuming events from where you left off the last time, set  <i>BookmarkXml</i> to the XML string that you persisted. For a subscription, pass the bookmark handle to the <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> function. For a query, pass the bookmark handle to the <a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a> function to seek to a specific event in the query result.

If the query is against multiple channels, the bookmark handle will contain bookmarks for each channel. You cannot create a bookmark for a log file.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the handle when done.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/e7eeafc3-deb9-4cdc-9763-f784db7333be">Bookmarking Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/aa31f0cf-b37a-40bb-922e-2b987b8a9dcf">EvtUpdateBookmark</a>
 

 

