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

# ISyncMgrHandler::GetName


## -description


Gets the display name of the handler.


## -parameters




### -param ppszName [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a <b>null</b>-terminated buffer that receives the handler name. The name can be of maximum length MAX_SYNCMGR_NAME, including the terminating <b>null</b> character. If the name exceeds that length, it is truncated.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The handler name is accessed as the System.DisplayName (PKEY_DisplayName) property in the Sync Center folder.

Sync Center calls this method any time that <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> or <a href="https://msdn.microsoft.com/752f197e-0dad-4b3d-9f70-352f5f50e9ee">UpdateHandlerCollection</a> is called. If <b>ISyncMgrHandler::GetName</b> fails or returns an empty string, the handler is not shown in the Sync Center folder and Sync Center will not attempt to invoke it.

It is the responsibility of the handler to allocate the string buffer using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Sync Center deallocates the buffer through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.

<b>ISyncMgrHandler::GetName</b> replaces the use of <a href="https://msdn.microsoft.com/bae3ead8-632c-45bf-a24e-bf07922039bd">GetHandlerInfo</a> to retrieve the handler name.



