---
UID: NF:syncmgr.ISyncMgrHandlerCollection.GetHandlerEnumerator
title: ISyncMgrHandlerCollection::GetHandlerEnumerator
author: windows-driver-content
description: Gets an enumerator that provides access to the IDs of sync handlers exposed to and managed by the user.
old-location: shell\ISyncMgrHandlerCollection_GetHandlerEnumerator.htm
old-project: shell
ms.assetid: 9324b621-b29f-47b1-a691-603cb96497e7
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetHandlerEnumerator, GetHandlerEnumerator method [Windows Shell], GetHandlerEnumerator method [Windows Shell],ISyncMgrHandlerCollection interface, ISyncMgrHandlerCollection interface [Windows Shell],GetHandlerEnumerator method, ISyncMgrHandlerCollection.GetHandlerEnumerator, ISyncMgrHandlerCollection::GetHandlerEnumerator, _shell_ISyncMgrHandlerCollection_GetHandlerEnumerator, shell.ISyncMgrHandlerCollection_GetHandlerEnumerator, syncmgr/ISyncMgrHandlerCollection::GetHandlerEnumerator
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrHandlerCollection.GetHandlerEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrHandlerCollection::GetHandlerEnumerator


## -description


Gets an enumerator that provides access to the IDs of sync handlers exposed to and managed by the user.


## -parameters




### -param ppenum [out]

Type: <b><a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>**</b>

When this method returns, contains an address of a pointer to an instance of <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> that enumerates the IDs of known sync handlers.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A sync handler ID is a string that uniquely represents the handler. The ID must be unique across all handlers in the system and is limited to a maximum length of <b>MAX_SYNCMGR_ID</b>, including the terminating null character.

Earlier versions of Windows relied on GUIDs to represent handler and item IDs. Windows Vista uses strings for their greater flexibility. It is still recommended that the string contain a GUID to ensure uniqueness, but it can also contain other information of use to the handler, specific to the application or device.



