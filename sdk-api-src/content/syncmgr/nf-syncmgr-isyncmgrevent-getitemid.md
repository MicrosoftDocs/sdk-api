---
UID: NF:syncmgr.ISyncMgrEvent.GetItemID
title: ISyncMgrEvent::GetItemID
author: windows-sdk-content
description: Gets the ID of the item for which the event was logged.
old-location: shell\ISyncMgrEvent_GetItemID.htm
old-project: shell
ms.assetid: 243f84eb-ad0b-44ac-bf61-53bb8b6e5af5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetItemID, GetItemID method [Windows Shell], GetItemID method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetItemID method, ISyncMgrEvent.GetItemID, ISyncMgrEvent::GetItemID, _shell_ISyncMgrEvent_GetItemID, shell.ISyncMgrEvent_GetItemID, syncmgr/ISyncMgrEvent::GetItemID
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrEvent.GetItemID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent::GetItemID


## -description


Gets the ID of the item for which the event was logged.


## -parameters




### -param ppszItemID [out]

Type: <b>LPWSTR*</b>

Contains a pointer to an item ID as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The item ID can have a maximum length of MAX_SYNCMGR_ID, including the terrminating null character. The event is expected to allocate the string buffer using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.



