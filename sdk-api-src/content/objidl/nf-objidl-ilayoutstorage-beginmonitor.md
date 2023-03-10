---
UID: NF:objidl.ILayoutStorage.BeginMonitor
title: ILayoutStorage::BeginMonitor (objidl.h)
description: The BeginMonitor method is used to begin monitoring when a loading operation is started. When the operation is complete, the application must call ILayoutStorage::EndMonitor.
helpviewer_keywords: ["BeginMonitor","BeginMonitor method [Structured Storage]","BeginMonitor method [Structured Storage]","ILayoutStorage interface","ILayoutStorage interface [Structured Storage]","BeginMonitor method","ILayoutStorage.BeginMonitor","ILayoutStorage::BeginMonitor","_stg_ilayoutstorage_beginmonitor","objidl/ILayoutStorage::BeginMonitor","stg.ilayoutstorage_beginmonitor"]
old-location: stg\ilayoutstorage_beginmonitor.htm
tech.root: Stg
ms.assetid: 16371d6c-adb9-43c2-80a4-377e94854bbb
ms.date: 12/05/2018
ms.keywords: BeginMonitor, BeginMonitor method [Structured Storage], BeginMonitor method [Structured Storage],ILayoutStorage interface, ILayoutStorage interface [Structured Storage],BeginMonitor method, ILayoutStorage.BeginMonitor, ILayoutStorage::BeginMonitor, _stg_ilayoutstorage_beginmonitor, objidl/ILayoutStorage::BeginMonitor, stg.ilayoutstorage_beginmonitor
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
 - ILayoutStorage::BeginMonitor
 - objidl/ILayoutStorage::BeginMonitor
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
 - ILayoutStorage.BeginMonitor
---

# ILayoutStorage::BeginMonitor


## -description

The <b>BeginMonitor</b> method is used to begin monitoring when a loading operation is started. When the operation is complete, the application must call 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-endmonitor">ILayoutStorage::EndMonitor</a>.



## -returns

This method supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as the following:

| Return code | Description |
|----------------|---------------|
| STG_E_INUSE | BeginMonitor</xref> was called while **ILayoutStorage** was already monitoring. |

## -remarks

Normally an application calls 
<b>BeginMonitor</b> before the actual loading begins. Once this method has been called, the compound file implementation regards any operation performed on the files storages and streams as part of the desired access pattern. The result is a layout script like that created explicitly by calling 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-layoutscript">ILayoutStorage::LayoutScript</a>.

Applications will usually use monitoring to obtain the access pattern of embedded objects. Monitoring also makes possible generic layout tools,  that launch existing applications and monitor their access patterns.

A call to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-endmonitor">ILayoutStorage::EndMonitor</a> ends monitoring. Multiple calls to 
<b>BeginMonitor</b> and
<b>EndMonitor</b> are permitted. Monitoring can also be mixed with calls to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-layoutscript">ILayoutStorage::LayoutScript</a>.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-endmonitor">ILayoutStorage::EndMonitor</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-layoutscript">ILayoutStorage::LayoutScript</a>
