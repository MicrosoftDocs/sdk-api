---
UID: NF:syncmgr.IEnumSyncMgrEvents.Next
title: IEnumSyncMgrEvents::Next
author: windows-sdk-content
description: Gets the next batch of events from the event store.
old-location: shell\IEnumSyncMgrEvents_Next.htm
tech.root: shell
ms.assetid: 22151b04-f4b8-46af-b55a-1ac2054900d3
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IEnumSyncMgrEvents interface [Windows Shell],Next method, IEnumSyncMgrEvents.Next, IEnumSyncMgrEvents::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumSyncMgrEvents interface, _shell_IEnumSyncMgrEvents_Next, shell.IEnumSyncMgrEvents_Next, syncmgr/IEnumSyncMgrEvents::Next
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
 - IEnumSyncMgrEvents.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSyncMgrEvents::Next


## -description


Gets the next batch of events from the event store.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

This value must be 1.


### -param rgelt [out]

Type: <b><a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a>**</b>

The address of an <a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a> interface pointer.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

A pointer to the number of events fetched.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



