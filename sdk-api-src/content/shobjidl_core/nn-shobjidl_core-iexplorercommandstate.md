---
UID: NN:shobjidl_core.IExplorerCommandState
title: IExplorerCommandState (shobjidl_core.h)
description: Exposes a single method that allows retrieval of the command state.
helpviewer_keywords: ["IExplorerCommandState","IExplorerCommandState interface [Windows Shell]","IExplorerCommandState interface [Windows Shell]","described","_shell_IExplorerCommandState","shell.IExplorerCommandState","shobjidl_core/IExplorerCommandState"]
old-location: shell\IExplorerCommandState.htm
tech.root: shell
ms.assetid: 020a6f6f-1d45-44bd-a57f-ef8000976b5b
ms.date: 12/05/2018
ms.keywords: IExplorerCommandState, IExplorerCommandState interface [Windows Shell], IExplorerCommandState interface [Windows Shell],described, _shell_IExplorerCommandState, shell.IExplorerCommandState, shobjidl_core/IExplorerCommandState
f1_keywords:
- shobjidl_core/IExplorerCommandState
dev_langs:
- c++
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
- IExplorerCommandState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExplorerCommandState interface


## -description


Exposes a single method that allows retrieval of the command state.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExplorerCommandState</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerCommandState</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommandstate-getstate">GetState</a>
</td>
<td align="left" width="63%">
Gets the command state associated with a specified Shell item.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface when you need to determine the command state dynamically (for instance, based on an item's properties). This interface provides the same functionality as <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getstate">IExplorerCommand::GetState</a>, without the overhead of that interface's additional methods. Implement <b>IExplorerCommandState</b> when you only need to compute the command state.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Do not call the method of <b>IExplorerCommandState</b> directly. Windows Explorer calls your <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommandstate-getstate">IExplorerCommandState::GetState</a> implementation when the user wants to perform an action on the item.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getstate">IExplorerCommand::GetState</a>
 

 

