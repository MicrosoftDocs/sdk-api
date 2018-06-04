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

# IDataTransferManagerInterop::ShowShareUIForWindow


## -description


Displays the UI for sharing content for the specified window.


## -parameters




### -param appWindow [in]

The window to show the share UI for.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is equivalent to the <a href="https://msdn.microsoft.com/70dc3f13-7374-41f3-9857-cdd99900c9f5">DataTransferManager.ShowShareUI</a> method, except that you specify a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/21a12246-a49e-4f1e-b539-c35164b488d7">DataTransferManager</a>



<a href="https://msdn.microsoft.com/70dc3f13-7374-41f3-9857-cdd99900c9f5">DataTransferManager.ShowShareUI</a>



<a href="https://msdn.microsoft.com/C4F49401-C863-4D3B-80EE-D36F714E7D90">IDataTransferManagerInterop</a>
 

 

