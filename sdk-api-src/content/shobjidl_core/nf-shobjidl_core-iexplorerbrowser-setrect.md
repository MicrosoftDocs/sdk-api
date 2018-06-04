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

# IExplorerBrowser::SetRect


## -description


Sets the size and position of the view windows created by the browser.


## -parameters




### -param phdwp [in, out]

Type: <b>HDWP*</b>

A pointer to a <a href="https://msdn.microsoft.com/2758de7b-c218-4a9b-b11b-b189301f7514">DeferWindowPos</a> handle. This parameter can be <b>NULL</b>.


### -param rcBrowser [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The coordinates that the browser will occupy.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Coordinates are relative to the <i>hwndParent</i> passed in <a href="https://msdn.microsoft.com/4b86646a-a20c-4bb5-a4c8-5c2e11e18862">IExplorerBrowser::Initialize</a>.



