---
UID: NF:syncmgr.ISyncMgrEventLinkUIOperation.Init
title: ISyncMgrEventLinkUIOperation::Init
author: windows-sdk-content
description: Enables Sync Center to provide the event to link to so ISyncMgrUIOperation::Run knows which event to operate upon.
old-location: shell\ISyncMgrEventLinkUIOperation_Init.htm
old-project: shell
ms.assetid: 6f9c9fd9-54f9-423d-af91-6f569a7c8616
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ISyncMgrEventLinkUIOperation interface [Windows Shell],Init method, ISyncMgrEventLinkUIOperation.Init, ISyncMgrEventLinkUIOperation::Init, Init, Init method [Windows Shell], Init method [Windows Shell],ISyncMgrEventLinkUIOperation interface, _shell_ISyncMgrEventLinkUIOperation_Init, shell.ISyncMgrEventLinkUIOperation_Init, syncmgr/ISyncMgrEventLinkUIOperation::Init
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrEventLinkUIOperation.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEventLinkUIOperation::Init


## -description


Enables Sync Center to provide the event to link to so <a href="https://msdn.microsoft.com/66dd853e-0fb0-4736-982a-e0183cb51842">ISyncMgrUIOperation::Run</a>  knows which event to operate upon.


## -parameters




### -param rguidEventID [in]

Type: <b>REFGUID</b>

A reference to the event ID that is being stored. This parameter is the same as what is returned from the <a href="https://msdn.microsoft.com/2951a015-b365-468b-a143-1b807885a99a">GetEventID</a> method of the <i>pEvent</i> parameter.


### -param pEvent [in]

Type: <b><a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a> object for <a href="https://msdn.microsoft.com/library/windows/hardware/ff569516">Run</a> to use. This is the event object that owns the link.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event ID is the ID that the handler is given when <a href="https://msdn.microsoft.com/4c7d6627-1652-4920-9dce-a61673e6e656">ReportEvent</a> is called, or is the ID provided by the handler when the event is obtained from the custom event store.

If you call <a href="https://msdn.microsoft.com/4c7d6627-1652-4920-9dce-a61673e6e656">ReportEvent</a>, your events will be stored only until the user logs off or until the handler is synchronized again.

The interface that is used to implement custom event stores is <a href="https://msdn.microsoft.com/218875bf-be6b-4ca5-8904-81c81c7fbf70">ISyncMgrEventStore</a>.

The <a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a> provided in the <i>pEvent</i> parameter is not the same object that came from a custom event store.



