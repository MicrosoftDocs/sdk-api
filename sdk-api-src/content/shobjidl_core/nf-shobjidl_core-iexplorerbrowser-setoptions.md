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



