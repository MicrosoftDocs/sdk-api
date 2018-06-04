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

# IPrintManagerInterop::ShowPrintUIForWindowAsync


## -description


Displays the UI for printing content for the specified window.


## -parameters




### -param appWindow [in]

The window to show the print UI  for.


### -param riid [in]

The reference ID of the specified window.


### -param asyncOperation [out, retval]

The asynchronous operation that reports completion.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can use the <b>ShowPrintUIForWindowAsync</b> method to show the print UI for the specified window. The <b>ShowPrintUIForWindowAsync</b> method is equivalent to the <a href="https://msdn.microsoft.com/74a7b687-909d-42f2-bb58-83b5be474d9c">ShowPrintUIAsync</a> method, except that you supply a reference to a window from a multi-window Windows Store app.




## -see-also




<a href="https://msdn.microsoft.com/1786fda1-37e4-4ec5-94de-a1fc5b6732a2">IPrintManagerInterop</a>



<a href="https://msdn.microsoft.com/81ad3b9b-36f2-46c0-8315-1d2bdfcebe75">PrintManager</a>



<a href="https://msdn.microsoft.com/74a7b687-909d-42f2-bb58-83b5be474d9c">ShowPrintUIAsync</a>
 

 

