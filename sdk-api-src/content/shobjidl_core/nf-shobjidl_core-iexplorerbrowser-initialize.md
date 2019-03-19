---
UID: NF:shobjidl_core.IExplorerBrowser.Initialize
title: IExplorerBrowser::Initialize (shobjidl_core.h)
author: windows-sdk-content
description: Prepares the browser to be navigated.
old-location: shell\IExplorerBrowser_Initialize.htm
tech.root: shell
ms.assetid: 4b86646a-a20c-4bb5-a4c8-5c2e11e18862
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],Initialize method, IExplorerBrowser.Initialize, IExplorerBrowser::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_Initialize, shell.IExplorerBrowser_Initialize, shobjidl_core/IExplorerBrowser::Initialize
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerBrowser::Initialize


## -description


Prepares the browser to be navigated.


## -parameters




### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the owner window or control.


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> that contains the coordinates of the bounding rectangle that the browser will occupy. The coordinates are relative to <i>hwndParent</i>.


### -param pfs [in]

Type: <b>const <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/be00fe39-1add-412e-b88b-4b0b1404b19d">FOLDERSETTINGS</a> structure that determines how the folder will be displayed in the view. If this parameter is <b>NULL</b>, then you must call <a href="https://msdn.microsoft.com/f24b98dd-18fc-495d-b7dd-d1491dc0a077">IExplorerBrowser::SetFolderSettings</a>; otherwise, the default view settings for the folder are used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After calling the <b>Initialize</b> method, it is the responsibility of the caller to call the <a href="https://msdn.microsoft.com/b6fc4aa6-f689-4b3e-a922-f8361d33b6dd">Destroy</a> method to destroy the browser and free any memory and windowed resources associated with the browser.



