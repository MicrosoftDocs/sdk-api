---
UID: NE:winevt._EVT_QUERY_PROPERTY_ID
title: EVT_QUERY_PROPERTY_ID (winevt.h)
description: Defines the identifiers that identify the query information that you can retrieve.
helpviewer_keywords: ["EVT_QUERY_PROPERTY_ID","EVT_QUERY_PROPERTY_ID enumeration [EventLog]","EvtQueryNames","EvtQueryPropertyIdEND","EvtQueryStatuses","wes.evt_query_property_id","winevt/EVT_QUERY_PROPERTY_ID","winevt/EvtQueryNames","winevt/EvtQueryPropertyIdEND","winevt/EvtQueryStatuses"]
old-location: wes\evt_query_property_id.htm
tech.root: wes
ms.assetid: 69a17378-088e-42e7-b7da-0ccc642f44d1
ms.date: 12/05/2018
ms.keywords: EVT_QUERY_PROPERTY_ID, EVT_QUERY_PROPERTY_ID enumeration [EventLog], EvtQueryNames, EvtQueryPropertyIdEND, EvtQueryStatuses, wes.evt_query_property_id, winevt/EVT_QUERY_PROPERTY_ID, winevt/EvtQueryNames, winevt/EvtQueryPropertyIdEND, winevt/EvtQueryStatuses
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
req.typenames: EVT_QUERY_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_QUERY_PROPERTY_ID
 - winevt/_EVT_QUERY_PROPERTY_ID
 - EVT_QUERY_PROPERTY_ID
 - winevt/EVT_QUERY_PROPERTY_ID
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
 - EVT_QUERY_PROPERTY_ID
---

# EVT_QUERY_PROPERTY_ID enumeration


## -description

Defines the identifiers that identify the query information that you can retrieve.

## -enum-fields

### -field EvtQueryNames

Identifies the property that contains the list of channel or log file names that are specified in the query. The variant type for this property is <b>EvtVarTypeString \| EVT_VARIANT_TYPE_ARRAY</b>.

### -field EvtQueryStatuses

Identifies the property that contains the list of Win32 error codes that correspond directly to the list of channel or log file names that the EvtQueryNames property returns. The error codes indicate the success or failure of the query for the specific channel or log file. The variant type for this property is <b>EvtVarTypeUInt32 \| EVT_VARIANT_TYPE_ARRAY</b>.

### -field EvtQueryPropertyIdEND

This enumeration value marks the end of the enumeration values.

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgetqueryinfo">EvtGetQueryInfo</a>