---
UID: NF:syncmgr.ISyncMgrHandlerCollection.GetHandlerEnumerator
title: ISyncMgrHandlerCollection::GetHandlerEnumerator (syncmgr.h)
description: Gets an enumerator that provides access to the IDs of sync handlers exposed to and managed by the user.
helpviewer_keywords: ["GetHandlerEnumerator","GetHandlerEnumerator method [Windows Shell]","GetHandlerEnumerator method [Windows Shell]","ISyncMgrHandlerCollection interface","ISyncMgrHandlerCollection interface [Windows Shell]","GetHandlerEnumerator method","ISyncMgrHandlerCollection.GetHandlerEnumerator","ISyncMgrHandlerCollection::GetHandlerEnumerator","_shell_ISyncMgrHandlerCollection_GetHandlerEnumerator","shell.ISyncMgrHandlerCollection_GetHandlerEnumerator","syncmgr/ISyncMgrHandlerCollection::GetHandlerEnumerator"]
old-location: shell\ISyncMgrHandlerCollection_GetHandlerEnumerator.htm
tech.root: shell
ms.assetid: 9324b621-b29f-47b1-a691-603cb96497e7
ms.date: 12/05/2018
ms.keywords: GetHandlerEnumerator, GetHandlerEnumerator method [Windows Shell], GetHandlerEnumerator method [Windows Shell],ISyncMgrHandlerCollection interface, ISyncMgrHandlerCollection interface [Windows Shell],GetHandlerEnumerator method, ISyncMgrHandlerCollection.GetHandlerEnumerator, ISyncMgrHandlerCollection::GetHandlerEnumerator, _shell_ISyncMgrHandlerCollection_GetHandlerEnumerator, shell.ISyncMgrHandlerCollection_GetHandlerEnumerator, syncmgr/ISyncMgrHandlerCollection::GetHandlerEnumerator
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
 - ISyncMgrHandlerCollection::GetHandlerEnumerator
 - syncmgr/ISyncMgrHandlerCollection::GetHandlerEnumerator
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
 - ISyncMgrHandlerCollection.GetHandlerEnumerator
---

# ISyncMgrHandlerCollection::GetHandlerEnumerator


## -description

Gets an enumerator that provides access to the IDs of sync handlers exposed to and managed by the user.

## -parameters

### -param ppenum [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>**</b>

When this method returns, contains an address of a pointer to an instance of <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> that enumerates the IDs of known sync handlers.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A sync handler ID is a string that uniquely represents the handler. The ID must be unique across all handlers in the system and is limited to a maximum length of <b>MAX_SYNCMGR_ID</b>, including the terminating null character.

Earlier versions of Windows relied on GUIDs to represent handler and item IDs. Windows Vista uses strings for their greater flexibility. It is still recommended that the string contain a GUID to ensure uniqueness, but it can also contain other information of use to the handler, specific to the application or device.