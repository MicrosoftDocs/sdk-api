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

# IFileDialog::Close


## -description


Closes the dialog.


## -parameters




### -param hr [in]

Type: <b>HRESULT</b>

The code that will be returned by <a href="https://msdn.microsoft.com/0284b694-64d1-48db-bef3-92f808b29b23">Show</a> to indicate that the dialog was closed before a selection was made.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application can call this method from a callback method or function while the dialog is open. The dialog will close and the <a href="https://msdn.microsoft.com/0284b694-64d1-48db-bef3-92f808b29b23">Show</a> method will return with the <b>HRESULT</b> specified in <i>hr</i>.

If this method is called, there is no result available for the <a href="https://msdn.microsoft.com/6572f172-8b66-4b42-b087-d0133595b380">IFileDialog::GetResult</a> or <a href="https://msdn.microsoft.com/5c710dae-4988-4f19-beb5-2ff9cd11c596">GetResults</a> methods, and they will fail if called.



