---
UID: NN:shobjidl.IResultsFolder
title: IResultsFolder (shobjidl.h)

description: Exposes methods that hold items from a data object.
old-location: shell\IResultsFolder.htm
tech.root: shell
ms.assetid: db44052b-bd26-412f-9f2a-66a0c53b65ac

ms.date: 12/05/2018
ms.keywords: IResultsFolder, IResultsFolder interface [Windows Shell], IResultsFolder interface [Windows Shell],described, _shell_IResultsFolder, shell.IResultsFolder, shobjidl/IResultsFolder
ms.topic: interface
f1_keywords: 
 - "shobjidl/IResultsFolder"
dev_langs:
 - c++
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Shobjidl.h
api_name:
 - IResultsFolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IResultsFolder interface


## -description


Exposes methods that hold items from a data object.

An <b>IResultsFolder</b> is a folder that can hold items from all over the namespace and represent them to the user in a single folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultsFolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultsFolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResultsFolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iresultsfolder-addidlist">AddIDList</a>
</td>
<td align="left" width="63%">
Inserts a PIDL into a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iresultsfolder-additem">AddItem</a>
</td>
<td align="left" width="63%">
Adds an item to a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iresultsfolder-removeall">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all items from a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iresultsfolder-removeidlist">RemoveIDList</a>
</td>
<td align="left" width="63%">
Removes a PIDL from a results folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/nf-shobjidl-iresultsfolder-removeitem">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes an item from a results folder.

</td>
</tr>
</table> 

