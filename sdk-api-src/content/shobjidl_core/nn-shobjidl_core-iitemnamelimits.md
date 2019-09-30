---
UID: NN:shobjidl_core.IItemNameLimits
title: IItemNameLimits (shobjidl_core.h)
author: windows-sdk-content
description: Retrieves a list of valid and invalid characters or the maximum length of a name in the namespace. Use this interface for validation parsing and translation.
old-location: shell\IItemNameLimits.htm
tech.root: shell
ms.assetid: 2850bdf1-12ea-42cd-a0fb-68491337ae69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IItemNameLimits, IItemNameLimits interface [Windows Shell], IItemNameLimits interface [Windows Shell],described, _shell_IItemNameLimits, shell.IItemNameLimits, shobjidl_core/IItemNameLimits
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IItemNameLimits"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IItemNameLimits interface


## -description


Retrieves a list of valid and invalid characters or the maximum length of a name in the namespace. Use this interface for validation parsing and translation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IItemNameLimits</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IItemNameLimits</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iitemnamelimits-getmaxlength">GetMaxLength</a>
</td>
<td align="left" width="63%">
Returns the maximum number of characters allowed for a particular name in the namespace under which it is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iitemnamelimits-getvalidcharacters">GetValidCharacters</a>
</td>
<td align="left" width="63%">
Loads a string that contains each of the characters that are valid or invalid in the namespace under which it is called.

</td>
</tr>
</table> 

