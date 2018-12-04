---
UID: NN:shobjidl_core.IItemNameLimits
title: IItemNameLimits
author: windows-sdk-content
description: Retrieves a list of valid and invalid characters or the maximum length of a name in the namespace. Use this interface for validation parsing and translation.
old-location: shell\IItemNameLimits.htm
tech.root: shell
ms.assetid: 2850bdf1-12ea-42cd-a0fb-68491337ae69
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IItemNameLimits, IItemNameLimits interface [Windows Shell], IItemNameLimits interface [Windows Shell],described, _shell_IItemNameLimits, shell.IItemNameLimits, shobjidl_core/IItemNameLimits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IItemNameLimits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IItemNameLimits interface


## -description


Retrieves a list of valid and invalid characters or the maximum length of a name in the namespace. Use this interface for validation parsing and translation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IItemNameLimits</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IItemNameLimits</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IItemNameLimits</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bf27218-8ad2-4268-a2e0-1ba36b0db4a3">GetMaxLength</a>
</td>
<td align="left" width="63%">
Returns the maximum number of characters allowed for a particular name in the namespace under which it is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6328be9-accd-4f11-82ee-49d3b18f9fd6">GetValidCharacters</a>
</td>
<td align="left" width="63%">
Loads a string that contains each of the characters that are valid or invalid in the namespace under which it is called.

</td>
</tr>
</table> 

