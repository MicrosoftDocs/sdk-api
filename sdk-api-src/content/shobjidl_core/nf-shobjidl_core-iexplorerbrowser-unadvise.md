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

# IExplorerBrowser::Unadvise


## -description


Terminates an advisory connection.


## -parameters




### -param dwCookie [in]

Type: <b>DWORD</b>

A connection token previously returned from <a href="https://msdn.microsoft.com/b77f9c41-248e-4f16-a9ff-6ff5437df11c">IExplorerBrowser::Advise</a>. Identifies the connection to be terminated.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Terminates an advisory connection previously established through method <a href="https://msdn.microsoft.com/b77f9c41-248e-4f16-a9ff-6ff5437df11c">IExplorerBrowser::Advise</a>. The <i>dwCookie</i> parameter identifies the connection to terminate. Failure to call  <b>IExplorerBrowser::Unadvise</b>, may result in a memory leak.



