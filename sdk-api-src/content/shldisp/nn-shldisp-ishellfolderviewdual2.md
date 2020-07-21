---
UID: NN:shldisp.IShellFolderViewDual2
title: IShellFolderViewDual2 (shldisp.h)
description: Exposes methods that modify the view and select items in the current folder.
helpviewer_keywords: ["IShellFolderViewDual2","IShellFolderViewDual2 interface [Windows Shell]","IShellFolderViewDual2 interface [Windows Shell]","described","_shell_IShellFolderViewDual2","shell.IShellFolderViewDual2","shldisp/IShellFolderViewDual2"]
old-location: shell\IShellFolderViewDual2.htm
tech.root: shell
ms.assetid: f53b779e-a015-4b17-b04d-e0739cba8168
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual2, IShellFolderViewDual2 interface [Windows Shell], IShellFolderViewDual2 interface [Windows Shell],described, _shell_IShellFolderViewDual2, shell.IShellFolderViewDual2, shldisp/IShellFolderViewDual2
f1_keywords:
- shldisp/IShellFolderViewDual2
dev_langs:
- c++
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
- Shldisp.h
api_name:
- IShellFolderViewDual2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolderViewDual2 interface


## -description


Exposes methods that modify the view and select items in the current folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderViewDual2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>. <b>IShellFolderViewDual2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderViewDual2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual2-get_currentviewmode">get_CurrentViewMode</a>
</td>
<td align="left" width="63%">
Gets the current view mode of the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual2-put_currentviewmode">put_CurrentViewMode</a>
</td>
<td align="left" width="63%">
Sets the current view mode of the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual2-selectitemrelative">SelectItemRelative</a>
</td>
<td align="left" width="63%">
Selects an item relative to the current item.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a> interface, from which it inherits.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>
 

 

