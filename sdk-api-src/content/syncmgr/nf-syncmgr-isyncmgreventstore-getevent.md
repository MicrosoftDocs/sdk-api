---
UID: NF:syncmgr.ISyncMgrEventStore.GetEvent
title: ISyncMgrEventStore::GetEvent
author: windows-sdk-content
description: Gets a specified event object.
old-location: shell\ISyncMgrEventStore_GetEvent.htm
tech.root: shell
ms.assetid: 6800ac62-1fd5-43a4-bd37-831449274a7b
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetEvent, GetEvent method [Windows Shell], GetEvent method [Windows Shell],ISyncMgrEventStore interface, ISyncMgrEventStore interface [Windows Shell],GetEvent method, ISyncMgrEventStore.GetEvent, ISyncMgrEventStore::GetEvent, _shell_ISyncMgrEventStore_GetEvent, shell.ISyncMgrEventStore_GetEvent, syncmgr/ISyncMgrEventStore::GetEvent
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrEventStore.GetEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrEventStore::GetEvent


## -description


Gets a specified event object.


## -parameters




### -param rguidEventID [in]

Type: <b>REFGUID</b>

A reference to event <b>GUID</b>.


### -param ppEvent [out]

Type: <b><a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a>**</b>

The address of <a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



