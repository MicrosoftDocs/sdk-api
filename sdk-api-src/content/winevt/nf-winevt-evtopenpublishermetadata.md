---
UID: NF:winevt.EvtOpenPublisherMetadata
title: EvtOpenPublisherMetadata function (winevt.h)
description: Gets a handle that you use to read the specified provider's metadata.
helpviewer_keywords: ["EvtOpenPublisherMetadata","EvtOpenPublisherMetadata function [EventLog]","wes.evtopenpublishermetadata","winevt/EvtOpenPublisherMetadata"]
old-location: wes\evtopenpublishermetadata.htm
tech.root: wes
ms.assetid: 0839fb15-12a9-4e30-9afa-6f6437956df0
ms.date: 12/05/2018
ms.keywords: EvtOpenPublisherMetadata, EvtOpenPublisherMetadata function [EventLog], wes.evtopenpublishermetadata, winevt/EvtOpenPublisherMetadata
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
 - EvtOpenPublisherMetadata
 - winevt/EvtOpenPublisherMetadata
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
 - Ext-MS-Win-WevtAPI-EventLog-L1-1-2.dll
api_name:
 - EvtOpenPublisherMetadata
---

# EvtOpenPublisherMetadata function


## -description

Gets a handle that you use to read the specified provider's metadata.

## -parameters

### -param Session [in, optional]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> to get the metadata for a provider on the local computer.

### -param PublisherId [in]

The name of the provider. To enumerate the names of the providers registered on the computer, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublisherenum">EvtOpenPublisherEnum</a> function.

### -param LogFilePath [in, optional]

The full path to an archived log file that contains the events that the provider logged. An archived log file also contains the provider's metadata. Use this parameter when the provider is not registered on the local computer. Set to <b>NULL</b> when reading the metadata from a registered provider..

### -param Locale [in]

The locale identifier to use when accessing the localized metadata from the provider. To create the locale identifier, use the MAKELCID macro. Set to 0 to use the locale identifier of the calling thread.

### -param Flags [in]

Reserved. Must be zero.

## -returns

If successful, the function returns a handle to the provider's metadata; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

 If you specify an archived log file, this function will check for the specified provider's metadata in the log file. If the provider's metadata is not found in the log file, the function will search for the provider in the list of registered providers on the local computer.

To read the provider's metadata, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a> function. To enumerate the events that the provider defines, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtopeneventmetadataenum">EvtOpenEventMetadataEnum</a> function.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the metadata handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtgetpublishermetadataproperty">EvtGetPublisherMetadataProperty</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtopeneventmetadataenum">EvtOpenEventMetadataEnum</a>



<a href="/windows/desktop/api/winevt/nf-winevt-evtopenpublisherenum">EvtOpenPublisherEnum</a>