---
UID: NF:objidl.ILayoutStorage.EndMonitor
title: ILayoutStorage::EndMonitor (objidl.h)
description: The EndMonitor method ends monitoring of a compound file. Must be preceded by a call to ILayoutStorage::BeginMonitor.
helpviewer_keywords: ["EndMonitor","EndMonitor method [Structured Storage]","EndMonitor method [Structured Storage]","ILayoutStorage interface","ILayoutStorage interface [Structured Storage]","EndMonitor method","ILayoutStorage.EndMonitor","ILayoutStorage::EndMonitor","_stg_ilayoutstorage_endmonitor","objidl/ILayoutStorage::EndMonitor","stg.ilayoutstorage_endmonitor"]
old-location: stg\ilayoutstorage_endmonitor.htm
tech.root: Stg
ms.assetid: 83b9486b-78b6-473c-9a9a-33f470a4d70f
ms.date: 12/05/2018
ms.keywords: EndMonitor, EndMonitor method [Structured Storage], EndMonitor method [Structured Storage],ILayoutStorage interface, ILayoutStorage interface [Structured Storage],EndMonitor method, ILayoutStorage.EndMonitor, ILayoutStorage::EndMonitor, _stg_ilayoutstorage_endmonitor, objidl/ILayoutStorage::EndMonitor, stg.ilayoutstorage_endmonitor
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILayoutStorage::EndMonitor
 - objidl/ILayoutStorage::EndMonitor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILayoutStorage.EndMonitor
---

# ILayoutStorage::EndMonitor


## -description

The <b>EndMonitor</b> method ends monitoring of a compound file. Must be preceded by a call to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-beginmonitor">ILayoutStorage::BeginMonitor</a>.



## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as all return values for <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

## -remarks

A call to 
<b>EndMonitor</b> is generally followed by a call to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-relayoutdocfile">ILayoutStorage::RelayoutDocfile</a>, which uses the access pattern detected by the monitoring to restructure the compound file.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-beginmonitor">ILayoutStorage::BeginMonitor</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-relayoutdocfile">ILayoutStorage::ReLayoutDocfile</a>
