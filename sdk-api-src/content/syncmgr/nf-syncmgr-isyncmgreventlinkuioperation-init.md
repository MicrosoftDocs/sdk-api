---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



