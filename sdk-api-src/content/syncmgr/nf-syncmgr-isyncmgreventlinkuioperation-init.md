---
UID: NF:syncmgr.ISyncMgrEventLinkUIOperation.Init
title: ISyncMgrEventLinkUIOperation::Init (syncmgr.h)
description: Enables Sync Center to provide the event to link to so ISyncMgrUIOperation::Run knows which event to operate upon.
helpviewer_keywords: ["ISyncMgrEventLinkUIOperation interface [Windows Shell]","Init method","ISyncMgrEventLinkUIOperation.Init","ISyncMgrEventLinkUIOperation::Init","Init","Init method [Windows Shell]","Init method [Windows Shell]","ISyncMgrEventLinkUIOperation interface","_shell_ISyncMgrEventLinkUIOperation_Init","shell.ISyncMgrEventLinkUIOperation_Init","syncmgr/ISyncMgrEventLinkUIOperation::Init"]
old-location: shell\ISyncMgrEventLinkUIOperation_Init.htm
tech.root: shell
ms.assetid: 6f9c9fd9-54f9-423d-af91-6f569a7c8616
ms.date: 12/05/2018
ms.keywords: ISyncMgrEventLinkUIOperation interface [Windows Shell],Init method, ISyncMgrEventLinkUIOperation.Init, ISyncMgrEventLinkUIOperation::Init, Init, Init method [Windows Shell], Init method [Windows Shell],ISyncMgrEventLinkUIOperation interface, _shell_ISyncMgrEventLinkUIOperation_Init, shell.ISyncMgrEventLinkUIOperation_Init, syncmgr/ISyncMgrEventLinkUIOperation::Init
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrEventLinkUIOperation::Init
 - syncmgr/ISyncMgrEventLinkUIOperation::Init
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrEventLinkUIOperation.Init
---

# ISyncMgrEventLinkUIOperation::Init


## -description

Enables Sync Center to provide the event to link to so <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgruioperation-run">ISyncMgrUIOperation::Run</a>  knows which event to operate upon.

## -parameters

### -param rguidEventID [in]

Type: <b>REFGUID</b>

A reference to the event ID that is being stored. This parameter is the same as what is returned from the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrevent-geteventid">GetEventID</a> method of the <i>pEvent</i> parameter.

### -param pEvent [in]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a>*</b>

A pointer to the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a> object for <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgruioperation-run">Run</a> to use. This is the event object that owns the link.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The event ID is the ID that the handler is given when <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportevent">ReportEvent</a> is called, or is the ID provided by the handler when the event is obtained from the custom event store.

If you call <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportevent">ReportEvent</a>, your events will be stored only until the user logs off or until the handler is synchronized again.

The interface that is used to implement custom event stores is <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgreventstore">ISyncMgrEventStore</a>.

The <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrevent">ISyncMgrEvent</a> provided in the <i>pEvent</i> parameter is not the same object that came from a custom event store.