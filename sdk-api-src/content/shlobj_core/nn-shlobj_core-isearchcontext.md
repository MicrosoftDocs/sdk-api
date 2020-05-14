---
UID: NN:shlobj_core.ISearchContext
title: ISearchContext (shlobj_core.h)
description: Exposes methods that channel customization information to the search hooks.helpviewer_keywords: ["ISearchContext","ISearchContext interface [Windows Shell]","ISearchContext interface [Windows Shell]","described","_shell_ISearchContext","shell.ISearchContext","shlobj_core/ISearchContext"]
old-location: shell\ISearchContext.htm
tech.root: shell
ms.assetid: 95ac188a-f27f-4e09-9de3-a822bbbd6e8e
ms.date: 12/05/2018
ms.keywords: ISearchContext, ISearchContext interface [Windows Shell], ISearchContext interface [Windows Shell],described, _shell_ISearchContext, shell.ISearchContext, shlobj_core/ISearchContext
f1_keywords:
- shlobj_core/ISearchContext
dev_langs:
- c++
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
- ISearchContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchContext interface


## -description


Exposes methods that channel customization information to the search hooks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchContext</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-isearchcontext-getsearchstyle">GetSearchStyle</a>
</td>
<td align="left" width="63%">
Overrides the registry settings that determine how an autosearch is performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-isearchcontext-getsearchtext">GetSearchText</a>
</td>
<td align="left" width="63%">
Retrieves the text that is in the browser's Address bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-isearchcontext-getsearchurl">GetSearchURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL that is being searched for.

</td>
</tr>
</table> 

