---
UID: NN:shldisp.IShellFolderViewDual3
title: IShellFolderViewDual3
author: windows-sdk-content
description: Exposes methods that modify the current folder view.
old-location: shell\IShellFolderViewDual3.htm
tech.root: shell
ms.assetid: 1aa70db8-4225-49de-8b8f-ec86b1aafa22
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IShellFolderViewDual3, IShellFolderViewDual3 interface [Windows Shell], IShellFolderViewDual3 interface [Windows Shell],described, _shell_IShellFolderViewDual3, shell.IShellFolderViewDual3, shldisp/IShellFolderViewDual3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderViewDual3 interface


## -description


Exposes methods that modify the current folder view.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderViewDual3</b> interface inherits from <a href="https://msdn.microsoft.com/f53b779e-a015-4b17-b04d-e0739cba8168">IShellFolderViewDual2</a>. <b>IShellFolderViewDual3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/60808015-317e-469f-aa28-a2c2bfdb16a8">FilterView</a>
</td>
<td align="left" width="63%">
Sets the filter on the contents of the current view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0fc82d4-d27e-4410-88a8-83839de8409b">get_FolderFlags</a>
</td>
<td align="left" width="63%">
Gets the settings for the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/144fa908-01d3-43f4-95e6-2aad62c23912">get_GroupBy</a>
</td>
<td align="left" width="63%">
Gets the column used for grouping the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/005c440f-2340-4965-b717-5aa0f4e5142f">get_IconSize</a>
</td>
<td align="left" width="63%">
Gets the icon size setting for the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9edad3e2-317f-4ff5-82fb-a816de5d2aa8">get_SortColumns</a>
</td>
<td align="left" width="63%">
Gets the names of the columns used to sort the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/698678a6-3624-420a-997a-9fd1e61d67e6">put_FolderFlags</a>
</td>
<td align="left" width="63%">
Sets the current folders settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32c23b6f-7c6f-432c-9f0e-11de8608e546">put_GroupBy</a>
</td>
<td align="left" width="63%">
Sets the column used in grouping the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6211ba0a-f65e-4940-a774-5800c41c24c5">put_IconSize</a>
</td>
<td align="left" width="63%">
Sets the icon size setting for the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd61c44e-1612-48e3-9230-1a3a4667ece6">put_SortColumns</a>
</td>
<td align="left" width="63%">
Sets the names of the columns to be sorted.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/48135f9d-ee80-4dec-87dc-83f407c25777">IShellFolderViewDual</a> and <a href="https://msdn.microsoft.com/f53b779e-a015-4b17-b04d-e0739cba8168">IShellFolderViewDual2</a> interfaces, from which it inherits.




## -see-also




<a href="https://msdn.microsoft.com/48135f9d-ee80-4dec-87dc-83f407c25777">IShellFolderViewDual</a>



<a href="https://msdn.microsoft.com/f53b779e-a015-4b17-b04d-e0739cba8168">IShellFolderViewDual2</a>
 

 

