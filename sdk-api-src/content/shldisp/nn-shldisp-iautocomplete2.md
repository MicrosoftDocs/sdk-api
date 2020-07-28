---
UID: NN:shldisp.IAutoComplete2
title: IAutoComplete2 (shldisp.h)
description: Extends IAutoComplete. This interface enables clients of the autocomplete object to retrieve and set a number of options that control how autocompletion operates.
helpviewer_keywords: ["IAutoComplete2","IAutoComplete2 interface [Windows Shell]","IAutoComplete2 interface [Windows Shell]","described","_win32_IAutoComplete2","shell.IAutoComplete2","shldisp/IAutoComplete2"]
old-location: shell\IAutoComplete2.htm
tech.root: shell
ms.assetid: c093719f-7176-4ba4-ae75-399e8beeebf0
ms.date: 12/05/2018
ms.keywords: IAutoComplete2, IAutoComplete2 interface [Windows Shell], IAutoComplete2 interface [Windows Shell],described, _win32_IAutoComplete2, shell.IAutoComplete2, shldisp/IAutoComplete2
f1_keywords:
- shldisp/IAutoComplete2
dev_langs:
- c++
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IAutoComplete2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAutoComplete2 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-iautocomplete">IAutoComplete</a>. This interface enables clients of the autocomplete object to retrieve and set a number of options that control how autocompletion operates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutoComplete2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-iautocomplete">IAutoComplete</a>. <b>IAutoComplete2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAutoComplete2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-iautocomplete2-getoptions">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the current autocomplete options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-iautocomplete2-setoptions">SetOptions</a>
</td>
<td align="left" width="63%">
Sets the current autocomplete options.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-iautocomplete">IAutoComplete</a> interface from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is not usually implemented by applications. It is exposed by the Shell's autocomplete object.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface when you need to retrieve or set autocomplete options. The list of available options is given in the method references.



