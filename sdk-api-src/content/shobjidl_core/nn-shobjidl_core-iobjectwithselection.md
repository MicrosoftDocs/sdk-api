---
UID: NN:shobjidl_core.IObjectWithSelection
title: IObjectWithSelection
author: windows-sdk-content
description: Exposes methods that get or set selected items represented by a Shell item array.
old-location: shell\IObjectWithSelection.htm
tech.root: shell
ms.assetid: 8fb248eb-73e7-4db0-8585-4accafe332d0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IObjectWithSelection, IObjectWithSelection interface [Windows Shell], IObjectWithSelection interface [Windows Shell],described, _shell_IObjectWithSelection, shell.IObjectWithSelection, shobjidl_core/IObjectWithSelection
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
 - IObjectWithSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithSelection interface


## -description


Exposes methods that get or set selected items represented by a Shell item array.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithSelection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectWithSelection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithSelection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc0c2c79-a475-4384-8255-809dc8bdb869">GetSelection</a>
</td>
<td align="left" width="63%">
Gets the Shell item array that contains the selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e561b8f8-36e9-45ec-beb2-62d7f429dec4">SetSelection</a>
</td>
<td align="left" width="63%">
Provides the Shell item array that specifies the items included in the selection.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented by verbs that implement <a href="https://msdn.microsoft.com/a3432f1a-dd33-4e0d-8b26-1312bb5151f7">IExecuteCommand</a>. This allows objects to invoke the verb on the selection through <a href="https://msdn.microsoft.com/388136bb-a5c0-48c0-adfc-f5154910fd72">IExecuteCommand::Execute</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
<b>IObjectWithSelection</b> is used by Windows Explorer to invoke a verb on the selected items. Do not call this interface directly.



