---
UID: NF:syncmgr.ISyncMgrControl.StopItemSync
title: ISyncMgrControl::StopItemSync
author: windows-sdk-content
description: Stops the synchronization of specified items managed by a particular handler.
old-location: shell\ISyncMgrControl_StopItemSync.htm
tech.root: shell
ms.assetid: dd56f26b-caae-4f4d-9a32-fac450e255d0
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],StopItemSync method, ISyncMgrControl.StopItemSync, ISyncMgrControl::StopItemSync, StopItemSync, StopItemSync method [Windows Shell], StopItemSync method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_StopItemSync, shell.ISyncMgrControl_StopItemSync, syncmgr/ISyncMgrControl::StopItemSync
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
 - ISyncMgrControl.StopItemSync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrControl::StopItemSync


## -description


Stops the synchronization of specified items managed by a particular handler.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

a pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param ppszItemIDs [in]

Type: <b>LPCWSTR*</b>

The address of a pointer to a buffer containing an array of IDs of the items to stop synchronizing. Each ID is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param cItems [in]

Type: <b>DWORD</b>

The number of IDs in <i>ppszItemIDs</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



