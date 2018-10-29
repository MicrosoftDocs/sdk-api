---
UID: NN:shldisp.IShellFolderViewDual2
title: IShellFolderViewDual2
author: windows-sdk-content
description: Exposes methods that modify the view and select items in the current folder.
old-location: shell\IShellFolderViewDual2.htm
tech.root: shell
ms.assetid: f53b779e-a015-4b17-b04d-e0739cba8168
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IShellFolderViewDual2, IShellFolderViewDual2 interface [Windows Shell], IShellFolderViewDual2 interface [Windows Shell],described, _shell_IShellFolderViewDual2, shell.IShellFolderViewDual2, shldisp/IShellFolderViewDual2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderViewDual2 interface


## -description


Exposes methods that modify the view and select items in the current folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderViewDual2</b> interface inherits from <a href="https://msdn.microsoft.com/48135f9d-ee80-4dec-87dc-83f407c25777">IShellFolderViewDual</a>. <b>IShellFolderViewDual2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/aa4bcb25-98f9-49c3-be25-abc6a5ecdcca">get_CurrentViewMode</a>
</td>
<td align="left" width="63%">
Gets the current view mode of the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80f0e24e-8104-472e-b1d9-58d42f3925fe">put_CurrentViewMode</a>
</td>
<td align="left" width="63%">
Sets the current view mode of the current folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/421a039e-49d6-4a93-958a-48c7e847fa6b">SelectItemRelative</a>
</td>
<td align="left" width="63%">
Selects an item relative to the current item.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/48135f9d-ee80-4dec-87dc-83f407c25777">IShellFolderViewDual</a> interface, from which it inherits.




## -see-also




<a href="https://msdn.microsoft.com/48135f9d-ee80-4dec-87dc-83f407c25777">IShellFolderViewDual</a>
 

 

