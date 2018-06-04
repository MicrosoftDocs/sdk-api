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

# IExplorerBrowser::Initialize


## -description


Prepares the browser to be navigated.


## -parameters




### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the owner window or control.


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> that contains the coordinates of the bounding rectangle that the browser will occupy. The coordinates are relative to <i>hwndParent</i>.


### -param pfs [in]

Type: <b>const <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> structure that determines how the folder will be displayed in the view. If this parameter is <b>NULL</b>, then you must call <a href="https://msdn.microsoft.com/f24b98dd-18fc-495d-b7dd-d1491dc0a077">IExplorerBrowser::SetFolderSettings</a>; otherwise, the default view settings for the folder are used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After calling the <b>Initialize</b> method, it is the responsibility of the caller to call the <a href="https://msdn.microsoft.com/b6fc4aa6-f689-4b3e-a922-f8361d33b6dd">Destroy</a> method to destroy the browser and free any memory and windowed resources associated with the browser.



