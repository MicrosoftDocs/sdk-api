---
UID: NF:winevt.EvtQuery
title: EvtQuery function (winevt.h)
author: windows-sdk-content
description: Runs a query to retrieve events from a channel or log file that match the specified query criteria.
old-location: wes\evtquery.htm
tech.root: wes
ms.assetid: 06b67ec4-74ab-47d7-b7b9-1180e7dee725
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EvtQuery, EvtQuery function [EventLog], wes.evtquery, winevt/EvtQuery
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
 - Ext-MS-Win-WevtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EvtQuery function


## -description


Runs a query to retrieve events from a channel or log file that match the specified query criteria.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://msdn.microsoft.com/26f1745c-dcca-4452-872e-1fffe20f049c">EvtOpenSession</a> function returns. Set to <b>NULL</b> to query for events on the local computer.


### -param Path [in]

The name of the channel or the full path to a log file that contains the events that you want to query. You can specify an .evt, .evtx, or.etl log file. The path is required if the <i>Query</i> parameter contains an XPath query; the path is ignored if the <i>Query</i> parameter contains a structured XML query and the query specifies the path.


### -param Query [in]

A query that specifies the types of events that you want to retrieve. You can specify an XPath 1.0 query or structured XML query. If your XPath contains more than 20 expressions, use a structured XML query. To receive all events, set this parameter to <b>NULL</b> or "*".


### -param Flags [in]

One or more flags that specify the order that you want to receive the events and whether you are querying against a channel or log file.  For possible values, see the <a href="https://msdn.microsoft.com/e4499356-f749-4cf9-9f5d-f6a701611f42">EVT_QUERY_FLAGS</a> enumeration.


## -returns



A handle to the query results if successful; otherwise, <b>NULL</b>. If the function returns <b>NULL</b>, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to get the error code.




## -remarks



  To get events from the query results, call the <a href="https://msdn.microsoft.com/46d40734-f022-4775-aa4f-13f4069c43c8">EvtNext</a> function. To retrieve events beginning with a specific event in the results, call the <a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a> function.

 You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function with the query results handle when done.

You must only use the query handle that this function returns on the same thread that created the handle.


#### Examples

For an example that shows how to use this function, see <a href="https://msdn.microsoft.com/929bedbf-6dce-428e-b2c0-de9dcfe4531b">Querying for Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/46d40734-f022-4775-aa4f-13f4069c43c8">EvtNext</a>



<a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a>



<a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a>
 

 

