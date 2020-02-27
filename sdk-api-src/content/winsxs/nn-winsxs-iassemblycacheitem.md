---
UID: NN:winsxs.IAssemblyCacheItem
title: IAssemblyCacheItem (winsxs.h)
description: The IAssemblyCacheItem interface can be used to install side-by-side assemblies into the side-by-side store using a stream-based installation.
old-location: setup\iassemblycacheitem.htm
tech.root: SbsCs
ms.assetid: 9df9ee58-0354-49f0-af9c-5b92179cfaea
ms.date: 12/05/2018
ms.keywords: IAssemblyCacheItem, IAssemblyCacheItem interface [Side-by-side Assemblies], IAssemblyCacheItem interface [Side-by-side Assemblies],described, setup.iassemblycacheitem, winsxs/IAssemblyCacheItem
f1_keywords:
- winsxs/IAssemblyCacheItem
dev_langs:
- c++
req.header: winsxs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Sxs.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sxs.dll
api_name:
- IAssemblyCacheItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAssemblyCacheItem interface


## -description


The <b>IAssemblyCacheItem</b> interface can be used to install side-by-side assemblies into the side-by-side store using a stream-based installation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssemblyCacheItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAssemblyCacheItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAssemblyCacheItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblycacheitem-commit">Commit</a>
</td>
<td align="left" width="63%">
Copies information into the side-by-side store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsxs/nf-winsxs-iassemblycacheitem-createstream">CreateStream</a>
</td>
<td align="left" width="63%">
Copies the source of a manifest or module into a stream.

</td>
</tr>
</table> 

