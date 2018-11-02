---
UID: NF:shobjidl_core.IExplorerBrowser.SetOptions
title: IExplorerBrowser::SetOptions
author: windows-sdk-content
description: Sets the current browser options.
old-location: shell\IExplorerBrowser_SetOptions.htm
tech.root: shell
ms.assetid: b2f8fe1b-afcd-4fb0-b96b-41e38c7fea0b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],SetOptions method, IExplorerBrowser.SetOptions, IExplorerBrowser::SetOptions, SetOptions, SetOptions method [Windows Shell], SetOptions method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_SetOptions, shell.IExplorerBrowser_SetOptions, shobjidl_core/IExplorerBrowser::SetOptions
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IExplorerBrowser.SetOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerBrowser::SetOptions


## -description


Sets the current browser options.


## -parameters




### -param dwFlag [in]

Type: <b><a href="https://msdn.microsoft.com/4e2983bc-cad2-4bcc-8169-57b5274b2142">EXPLORER_BROWSER_OPTIONS</a></b>

One or more <a href="https://msdn.microsoft.com/4e2983bc-cad2-4bcc-8169-57b5274b2142">EXPLORER_BROWSER_OPTIONS</a> flags to be set.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This action overrides any previous options.

Frames are disabled by default. To enable frames and get the default set of panes, set the <a href="https://msdn.microsoft.com/4e2983bc-cad2-4bcc-8169-57b5274b2142">EBO_SHOWFRAMES</a> flag using the <b>SetOptions</b> method. The default panes, listed as <a href="https://msdn.microsoft.com/b940adc2-dfef-49c5-b86c-d0da83db0aad">IExplorerPaneVisibility</a> constants, are these: 

                

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
See <a href="https://msdn.microsoft.com/6c051cdc-b7f9-48dc-ba32-38f0f1ee5fda">IExplorerPaneVisibility::GetPaneState</a> for more information.



