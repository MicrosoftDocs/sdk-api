---
UID: NN:shobjidl.IAutoCompleteDropDown
title: IAutoCompleteDropDown
author: windows-sdk-content
description: Exposes methods that allow clients to reset or query the display state of the autocomplete drop-down list, which contains possible completions to a string entered by the user in an edit control.
old-location: shell\IAutoCompleteDropDown.htm
tech.root: shell
ms.assetid: 1f956d61-6a09-464e-bfe8-0b3bcb9ea181
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IAutoCompleteDropDown, IAutoCompleteDropDown interface [Windows Shell], IAutoCompleteDropDown interface [Windows Shell],described, _shell_IAutoCompleteDropDown, shell.IAutoCompleteDropDown, shobjidl/IAutoCompleteDropDown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Browseui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Browseui.dll
api_name:
 - IAutoCompleteDropDown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutoCompleteDropDown interface


## -description


Exposes methods that allow clients to reset or query the display state of the autocomplete drop-down list, which contains possible completions to a string entered by the user in an edit control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutoCompleteDropDown</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAutoCompleteDropDown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAutoCompleteDropDown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/824c435c-e8ee-4435-a779-bae3ef721613">GetDropDownStatus</a>
</td>
<td align="left" width="63%">
Gets the current display status of the autocomplete drop-down list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a880b2a-190a-45ea-8672-f2d0247987ed">ResetEnumerator</a>
</td>
<td align="left" width="63%">
Forces the autocomplete object to refresh its list of suggestions when the list is visible.

</td>
</tr>
</table> 

