---
UID: NE:winevt._EVT_QUERY_FLAGS
title: EVT_QUERY_FLAGS (winevt.h)
description: Defines the values that specify how to return the query results and whether you are query against a channel or log file.
helpviewer_keywords: ["EVT_QUERY_FLAGS","EVT_QUERY_FLAGS enumeration [EventLog]","EvtQueryChannelPath","EvtQueryFilePath","EvtQueryForwardDirection","EvtQueryReverseDirection","EvtQueryTolerateQueryErrors","wes.evt_query_flags","winevt/EVT_QUERY_FLAGS","winevt/EvtQueryChannelPath","winevt/EvtQueryFilePath","winevt/EvtQueryForwardDirection","winevt/EvtQueryReverseDirection","winevt/EvtQueryTolerateQueryErrors"]
old-location: wes\evt_query_flags.htm
tech.root: wes
ms.assetid: e4499356-f749-4cf9-9f5d-f6a701611f42
ms.date: 12/05/2018
ms.keywords: EVT_QUERY_FLAGS, EVT_QUERY_FLAGS enumeration [EventLog], EvtQueryChannelPath, EvtQueryFilePath, EvtQueryForwardDirection, EvtQueryReverseDirection, EvtQueryTolerateQueryErrors, wes.evt_query_flags, winevt/EVT_QUERY_FLAGS, winevt/EvtQueryChannelPath, winevt/EvtQueryFilePath, winevt/EvtQueryForwardDirection, winevt/EvtQueryReverseDirection, winevt/EvtQueryTolerateQueryErrors
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EVT_QUERY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_QUERY_FLAGS
 - winevt/_EVT_QUERY_FLAGS
 - EVT_QUERY_FLAGS
 - winevt/EVT_QUERY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_QUERY_FLAGS
---

# EVT_QUERY_FLAGS enumeration


## -description

Defines the values that specify how to return the query results and whether you are query against a channel or log file.

## -enum-fields

### -field EvtQueryChannelPath:0x1

Specifies that the query is against one or more channels. The <i>Path</i> parameter of the <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> function must specify the name of a  channel or <b>NULL</b>.

### -field EvtQueryFilePath:0x2

Specifies that the query is against one or more log files. The <i>Path</i> parameter of the <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> function must specify the full path to a log file or <b>NULL</b>.

### -field EvtQueryForwardDirection:0x100

Specifies that the events in the query result are ordered from oldest to newest. This is the default.

### -field EvtQueryReverseDirection:0x200

Specifies that the events in the query result are ordered from newest to oldest.

### -field EvtQueryTolerateQueryErrors:0x1000

Specifies that <a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a> should run the query even if the part of the query generates an error (is not well formed). The service validates the syntax of the XPath query to determine if it is well formed. If the validation fails, the service parses the XPath into individual expressions. It builds a new XPath beginning with the left most expression. The service validates the expression and if it is valid, the service adds the next expression to the XPath. The service repeats this process until it finds the expression that is failing. It then uses the valid expressions that it found beginning with the leftmost expression as the XPath query (which means that you may not get the events that you expected). If no part of the XPath is valid, the <b>EvtQuery</b> call fails.

## -remarks

The EvtQueryChannelPath and EvtQueryFilePath flags are mutually exclusive. The EvtQueryForwardDirection and EvtQueryReverseDirection flags are also mutually exclusive.

You can retrieve events only in a forward direction from Debug and Analytic channels and from .evt and .etl log files.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtquery">EvtQuery</a>
