---
UID: NN:shobjidl_core.IExplorerCommandState
title: IExplorerCommandState
author: windows-sdk-content
description: Exposes a single method that allows retrieval of the command state.
old-location: shell\IExplorerCommandState.htm
old-project: shell
ms.assetid: 020a6f6f-1d45-44bd-a57f-ef8000976b5b
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IExplorerCommandState, IExplorerCommandState interface [Windows Shell], IExplorerCommandState interface [Windows Shell],described, _shell_IExplorerCommandState, shell.IExplorerCommandState, shobjidl_core/IExplorerCommandState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IExplorerCommandState
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IExplorerCommandState interface


## -description


Exposes a single method that allows retrieval of the command state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerCommandState</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExplorerCommandState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExplorerCommandState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a93bc6af-bea3-48c1-b3bd-a2bb2a0582a7">GetState</a>
</td>
<td align="left" width="63%">
Gets the command state associated with a specified Shell item.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface when you need to determine the command state dynamically (for instance, based on an item's properties). This interface provides the same functionality as <a href="https://msdn.microsoft.com/bb600cb5-9b7e-45dc-beca-0a913c214084">IExplorerCommand::GetState</a>, without the overhead of that interface's additional methods. Implement <b>IExplorerCommandState</b> when you only need to compute the command state.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Do not call the method of <b>IExplorerCommandState</b> directly. Windows Explorer calls your <a href="https://msdn.microsoft.com/a93bc6af-bea3-48c1-b3bd-a2bb2a0582a7">IExplorerCommandState::GetState</a> implementation when the user wants to perform an action on the item.




## -see-also




<a href="https://msdn.microsoft.com/bb600cb5-9b7e-45dc-beca-0a913c214084">IExplorerCommand::GetState</a>
 

 

