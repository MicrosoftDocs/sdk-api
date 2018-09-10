---
UID: NN:winsxs.IAssemblyCacheItem
title: IAssemblyCacheItem
author: windows-sdk-content
description: The IAssemblyCacheItem interface can be used to install side-by-side assemblies into the side-by-side store using a stream-based installation.
old-location: setup\iassemblycacheitem.htm
tech.root: SbsCs
ms.assetid: 9df9ee58-0354-49f0-af9c-5b92179cfaea
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IAssemblyCacheItem, IAssemblyCacheItem interface [Side-by-side Assemblies], IAssemblyCacheItem interface [Side-by-side Assemblies],described, setup.iassemblycacheitem, winsxs/IAssemblyCacheItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAssemblyCacheItem interface


## -description


The <b>IAssemblyCacheItem</b> interface can be used to install side-by-side assemblies into the side-by-side store using a stream-based installation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAssemblyCacheItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAssemblyCacheItem</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d8f8b6b3-72b4-400b-a780-fc25d1f4b9d0">Commit</a>
</td>
<td align="left" width="63%">
Copies information into the side-by-side store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b3726cc-91c2-4614-a3a7-3f89f201e04a">CreateStream</a>
</td>
<td align="left" width="63%">
Copies the source of a manifest or module into a stream.

</td>
</tr>
</table> 

