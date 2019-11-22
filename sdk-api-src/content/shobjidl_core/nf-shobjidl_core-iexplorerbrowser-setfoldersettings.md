---
UID: NF:shobjidl_core.IExplorerBrowser.SetFolderSettings
title: IExplorerBrowser::SetFolderSettings (shobjidl_core.h)

description: Sets the folder settings for the current view.
old-location: shell\IExplorerBrowser_SetFolderSettings.htm
tech.root: shell
ms.assetid: f24b98dd-18fc-495d-b7dd-d1491dc0a077

ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],SetFolderSettings method, IExplorerBrowser.SetFolderSettings, IExplorerBrowser::SetFolderSettings, SetFolderSettings, SetFolderSettings method [Windows Shell], SetFolderSettings method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_SetFolderSettings, shell.IExplorerBrowser_SetFolderSettings, shobjidl_core/IExplorerBrowser::SetFolderSettings
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IExplorerBrowser.SetFolderSettings"
dev_langs:
 - c++
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
 - IExplorerBrowser.SetFolderSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerBrowser::SetFolderSettings


## -description


Sets the folder settings for the current view.


## -parameters




### -param pfs [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> structure that contains the folder settings to be applied.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method also changes the default that will be applied when navigating to another location.

To ensure the view state is perserved across sessions, specify the persistence name using <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setpropertybag">IExplorerBrowser::SetPropertyBag</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a>
 

 

