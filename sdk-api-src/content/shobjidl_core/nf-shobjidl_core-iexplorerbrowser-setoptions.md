---
UID: NF:shobjidl_core.IExplorerBrowser.SetOptions
title: IExplorerBrowser::SetOptions (shobjidl_core.h)
description: Sets the current browser options.
helpviewer_keywords: ["IExplorerBrowser interface [Windows Shell]","SetOptions method","IExplorerBrowser.SetOptions","IExplorerBrowser::SetOptions","SetOptions","SetOptions method [Windows Shell]","SetOptions method [Windows Shell]","IExplorerBrowser interface","_shell_IExplorerBrowser_SetOptions","shell.IExplorerBrowser_SetOptions","shobjidl_core/IExplorerBrowser::SetOptions"]
old-location: shell\IExplorerBrowser_SetOptions.htm
tech.root: shell
ms.assetid: b2f8fe1b-afcd-4fb0-b96b-41e38c7fea0b
ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],SetOptions method, IExplorerBrowser.SetOptions, IExplorerBrowser::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_SetOptions, shell.IExplorerBrowser_SetOptions, shobjidl_core/IExplorerBrowser::SetOptions
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExplorerBrowser::SetOptions
 - shobjidl_core/IExplorerBrowser::SetOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.SetOptions
---

# IExplorerBrowser::SetOptions


## -description

Sets the current browser options.

## -parameters

### -param dwFlag [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options">EXPLORER_BROWSER_OPTIONS</a></b>

One or more <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options">EXPLORER_BROWSER_OPTIONS</a> flags to be set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This action overrides any previous options.

Frames are disabled by default. To enable frames and get the default set of panes, set the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options">EBO_SHOWFRAMES</a> flag using the <b>SetOptions</b> method. The default panes, listed as <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility">IExplorerPaneVisibility</a> constants, are these: 

                

<ul>
<li>EP_NavPane</li>
<li>EP_Commands</li>
<li>EP_Commands_Organize</li>
<li>EP_Commands_View</li>
<li>EP_DetailsPane</li>
<li>EP_PreviewPane</li>
<li>EP_QueryPane</li>
<li>EP_AdvQueryPane</li>
<li>EP_StatusBar</li>
<li>EP_Ribbon</li>
</ul>
See <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate">IExplorerPaneVisibility::GetPaneState</a> for more information.