---
UID: NF:winevt.EvtOpenEventMetadataEnum
title: EvtOpenEventMetadataEnum function (winevt.h)
description: Gets a handle that you use to enumerate the list of events that the provider defines.
helpviewer_keywords: ["EvtOpenEventMetadataEnum","EvtOpenEventMetadataEnum function [EventLog]","wes.evtopeneventmetadataenum","winevt/EvtOpenEventMetadataEnum"]
old-location: wes\evtopeneventmetadataenum.htm
tech.root: wes
ms.assetid: e1d2e5d5-89db-4bda-9803-37f26d1fe30f
ms.date: 12/05/2018
ms.keywords: EvtOpenEventMetadataEnum, EvtOpenEventMetadataEnum function [EventLog], wes.evtopeneventmetadataenum, winevt/EvtOpenEventMetadataEnum
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
 - EvtOpenEventMetadataEnum
 - winevt/EvtOpenEventMetadataEnum
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
 - EvtOpenEventMetadataEnum
---

# EvtOpenEventMetadataEnum function


## -description

Gets a handle that you use to enumerate the list of events that the provider defines.

## -parameters

### -param PublisherMetadata [in]

A handle to the provider's metadata that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublishermetadata">EvtOpenPublisherMetadata</a> function returns.

### -param Flags [in]

Reserved. Must be zero.

## -returns

If successful, the function returns a handle to the list of events that the  provider defines; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

To enumerate the events, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtnexteventmetadata">EvtNextEventMetadata</a> function in a loop.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the enumerator handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgeteventmetadataproperty">EvtGetEventMetadataProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtnexteventmetadata">EvtNextEventMetadata</a>