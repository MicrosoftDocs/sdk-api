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

# IRemoteComputer::Initialize


## -description


Used by Windows Explorer or Windows Internet Explorer when it is initializing or enumerating a namespace extension invoked on a remote computer.


## -parameters




### -param pszMachine

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the machine name of the remote computer.


### -param bEnumerating

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if Windows Explorer is enumerating the namespace extension, or <b>FALSE</b> if it is initializing it.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or standard OLE error values otherwise.




## -remarks



If failure is returned, the extension won't appear for the specified computer. Otherwise, the extension will appear and target the remote computer.



