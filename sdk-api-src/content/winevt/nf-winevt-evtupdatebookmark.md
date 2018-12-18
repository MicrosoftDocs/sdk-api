---
UID: NF:winevt.EvtUpdateBookmark
title: EvtUpdateBookmark function
author: windows-sdk-content
description: Updates the bookmark with information that identifies the specified event.
old-location: wes\evtupdatebookmark.htm
tech.root: wes
ms.assetid: aa31f0cf-b37a-40bb-922e-2b987b8a9dcf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EvtUpdateBookmark, EvtUpdateBookmark function [EventLog], wes.evtupdatebookmark, winevt/EvtUpdateBookmark
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
 - EvtUpdateBookmark
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtUpdateBookmark function


## -description


Updates the bookmark with information that identifies the specified event.


## -parameters




### -param Bookmark [in]

The handle to the bookmark to be updated. The <a href="https://msdn.microsoft.com/1020d923-090b-48fc-96c2-394db5cd241e">EvtCreateBookmark</a> function returns this handle.


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
The function failed. Call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1020d923-090b-48fc-96c2-394db5cd241e">EvtCreateBookmark</a>
 

 

