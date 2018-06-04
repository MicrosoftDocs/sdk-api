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

# ISyncMgrSyncCallback::SetHandlerProgressText


## -description


Sets the content of an information field for the handler while that handler is performing a synchronization.


## -parameters




### -param pszProgressText [in]

Type: <b>LPCWSTR</b>

Pointer to a buffer containing the comment text.


### -param pnCancelRequest [in, out]

Type: <b><a href="https://msdn.microsoft.com/81cf8dcc-c847-41e0-82e2-b5f547fc03cf">SYNCMGR_CANCEL_REQUEST</a>*</b>

A value from the <a href="https://msdn.microsoft.com/81cf8dcc-c847-41e0-82e2-b5f547fc03cf">SYNCMGR_CANCEL_REQUEST</a> enumeration specifying the nature of a cancel request, if any.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



