---
UID: NF:winevt.EvtOpenPublisherEnum
title: EvtOpenPublisherEnum function (winevt.h)
description: Gets a handle that you use to enumerate the list of registered providers on the computer.
helpviewer_keywords: ["EvtOpenPublisherEnum","EvtOpenPublisherEnum function [EventLog]","wes.evtopenpublisherenum","winevt/EvtOpenPublisherEnum"]
old-location: wes\evtopenpublisherenum.htm
tech.root: wes
ms.assetid: 156c434c-6d0f-4af0-bf10-20aa6bae0945
ms.date: 12/05/2018
ms.keywords: EvtOpenPublisherEnum, EvtOpenPublisherEnum function [EventLog], wes.evtopenpublisherenum, winevt/EvtOpenPublisherEnum
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
 - EvtOpenPublisherEnum
 - winevt/EvtOpenPublisherEnum
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
 - EvtOpenPublisherEnum
---

# EvtOpenPublisherEnum function


## -description

Gets a handle that you use to enumerate the list of registered providers on the computer.

## -parameters

### -param Session [in]

A remote session handle that the <a href="/windows/desktop/api/winevt/nf-winevt-evtopensession">EvtOpenSession</a> function returns. Set to <b>NULL</b> to enumerate the registered providers on the local computer.

### -param Flags [in]

Reserved. Must be zero.

## -returns

If successful, the function returns a handle to the list of registered providers; otherwise, <b>NULL</b>. If <b>NULL</b>, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to get the error code.

## -remarks

To enumerate the registered providers, call the <a href="/windows/desktop/api/winevt/nf-winevt-evtnextpublisherid">EvtNextPublisherId</a> function in a loop.

You must call the <a href="/windows/desktop/api/winevt/nf-winevt-evtclose">EvtClose</a> function to close the enumerator handle when done.


#### Examples

For an example that shows how to use this function, see <a href="/windows/desktop/WES/getting-a-provider-s-metadata-">Getting a Provider's Metadata</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winevt/nf-winevt-evtnextpublisherid">EvtNextPublisherId</a>