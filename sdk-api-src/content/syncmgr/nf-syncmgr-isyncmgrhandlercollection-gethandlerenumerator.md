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



