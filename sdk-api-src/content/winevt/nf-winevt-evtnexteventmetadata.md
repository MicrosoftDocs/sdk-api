---
UID: NF:winevt.EvtNextEventMetadata
title: EvtNextEventMetadata function (winevt.h)
description: Gets an event definition from the enumerator.
helpviewer_keywords: ["EvtNextEventMetadata","EvtNextEventMetadata function [EventLog]","wes.evtnexteventmetadata","winevt/EvtNextEventMetadata"]
old-location: wes\evtnexteventmetadata.htm
tech.root: wes
ms.assetid: 1077dc7c-3e73-4135-9020-20d086e30e71
ms.date: 12/05/2018
ms.keywords: EvtNextEventMetadata, EvtNextEventMetadata function [EventLog], wes.evtnexteventmetadata, winevt/EvtNextEventMetadata
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
 - EvtNextEventMetadata
 - winevt/EvtNextEventMetadata
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
 - EvtNextEventMetadata
---

# EvtNextEventMetadata function


## -description

Gets an event definition from the enumerator.

## -parameters

### -param EventMetadataEnum [in]

A handle to the event definition enumerator that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopeneventmetadataenum">EvtOpenEventMetadataEnum</a> function returns.

### -param Flags [in]

Reserved. Must be zero.

## -returns

If successful, the function returns a handle to the event's metadata; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

Call this function in a loop until the function returns <b>NULL</b> and the error code is ERROR_NO_MORE_ITEMS.

To get a property from the event definition, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgeteventmetadataproperty">EvtGetEventMetadataProperty</a> function.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the event definition handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgeteventmetadataproperty">EvtGetEventMetadataProperty</a>