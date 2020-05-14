---
UID: NF:winevt.EvtQuery
title: EvtQuery function (winevt.h)
description: Runs a query to retrieve events from a channel or log file that match the specified query criteria.helpviewer_keywords: ["EvtQuery","EvtQuery function [EventLog]","wes.evtquery","winevt/EvtQuery"]
old-location: wes\evtquery.htm
tech.root: wes
ms.assetid: 06b67ec4-74ab-47d7-b7b9-1180e7dee725
ms.date: 12/05/2018
ms.keywords: EvtQuery, EvtQuery function [EventLog], wes.evtquery, winevt/EvtQuery
f1_keywords:
- winevt/EvtQuery
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EvtQuery function


## -description


Runs a query to retrieve events from a channel or log file that match the specified query criteria.


## -parameters




### -param Session [in]

A remote session handle that the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> to query for events on the local computer.


### -param Path [in]

The name of the channel or the full path to a log file that contains the events that you want to query. You can specify an .evt, .evtx, or.etl log file. The path is required if the <i>Query</i> parameter contains an XPath query; the path is ignored if the <i>Query</i> parameter contains a structured XML query and the query specifies the path.


### -param Query [in]

A query that specifies the types of events that you want to retrieve. You can specify an XPath 1.0 query or structured XML query. If your XPath contains more than 20 expressions, use a structured XML query. To receive all events, set this parameter to <b>NULL</b> or "*".


### -param Flags [in]

One or more flags that specify the order that you want to receive the events and whether you are querying against a channel or log file.  For possible values, see the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/ne-winevt-evt_query_flags">EVT_QUERY_FLAGS</a> enumeration.


## -returns



A handle to the query results if successful; otherwise, <b>NULL</b>. If the function returns <b>NULL</b>, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.




## -remarks



  To get events from the query results, call the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtnext">EvtNext</a> function. To retrieve events beginning with a specific event in the results, call the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a> function.

 You must call the <a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function with the query results handle when done.

You must only use the query handle that this function returns on the same thread that created the handle.


#### Examples

For an example that shows how to use this function, see <a href="https://docs.microsoft.com/windows/desktop/WES/querying-for-events">Querying for Events</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtnext">EvtNext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtseek">EvtSeek</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winevt/nf-winevt-evtsubscribe">EvtSubscribe</a>
 

 

