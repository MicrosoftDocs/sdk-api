---
UID: NN:shldisp.IShellFolderViewDual3
title: IShellFolderViewDual3 (shldisp.h)
description: Exposes methods that modify the current folder view.
helpviewer_keywords: ["IShellFolderViewDual3","IShellFolderViewDual3 interface [Windows Shell]","IShellFolderViewDual3 interface [Windows Shell]","described","_shell_IShellFolderViewDual3","shell.IShellFolderViewDual3","shldisp/IShellFolderViewDual3"]
old-location: shell\IShellFolderViewDual3.htm
tech.root: shell
ms.assetid: 1aa70db8-4225-49de-8b8f-ec86b1aafa22
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual3, IShellFolderViewDual3 interface [Windows Shell], IShellFolderViewDual3 interface [Windows Shell],described, _shell_IShellFolderViewDual3, shell.IShellFolderViewDual3, shldisp/IShellFolderViewDual3
f1_keywords:
- shldisp/IShellFolderViewDual3
dev_langs:
- c++
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- IShellFolderViewDual3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolderViewDual3 interface


## -description


Exposes methods that modify the current folder view.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderViewDual3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>. <b>IShellFolderViewDual3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderViewDual3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-filterview">FilterView</a>
</td>
<td align="left" width="63%">
Sets the filter on the contents of the current view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-get_folderflags">get_FolderFlags</a>
</td>
<td align="left" width="63%">
Gets the settings for the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-get_groupby">get_GroupBy</a>
</td>
<td align="left" width="63%">
Gets the column used for grouping the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-get_iconsize">get_IconSize</a>
</td>
<td align="left" width="63%">
Gets the icon size setting for the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-get_sortcolumns">get_SortColumns</a>
</td>
<td align="left" width="63%">
Gets the names of the columns used to sort the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-put_folderflags">put_FolderFlags</a>
</td>
<td align="left" width="63%">
Sets the current folders settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-put_groupby">put_GroupBy</a>
</td>
<td align="left" width="63%">
Sets the column used in grouping the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-put_iconsize">put_IconSize</a>
</td>
<td align="left" width="63%">
Sets the icon size setting for the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual3-put_sortcolumns">put_SortColumns</a>
</td>
<td align="left" width="63%">
Sets the names of the columns to be sorted.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a> interfaces, from which it inherits.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>
 

 

