---
UID: NN:shobjidl_core.IDelegateFolder
title: IDelegateFolder
author: windows-sdk-content
description: Exposes a method through which a delegate folder is given the IMalloc interface required to allocate and free item IDs.
old-location: shell\IDelegateFolder.htm
old-project: shell
ms.assetid: 16db01f3-4167-43f0-9ef7-34eec906e199
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IDelegateFolder, IDelegateFolder interface [Windows Shell], IDelegateFolder interface [Windows Shell],described, shell.IDelegateFolder, shell_IDelegateFolder, shobjidl_core/IDelegateFolder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDelegateFolder
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IDelegateFolder interface


## -description


Exposes a method through which a delegate folder is given the <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface required to allocate and free item IDs.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDelegateFolder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDelegateFolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDelegateFolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce1ee472-e245-4112-858a-1d9739f5a36d">SetItemAlloc</a>
</td>
<td align="left" width="63%">
Provides the delegate folder an <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> interface used to allocate and free item IDs.

</td>
</tr>
</table> 


## -remarks



The IDs allocated by the delegate folder are in the form of <a href="https://msdn.microsoft.com/986591cf-97c5-4328-900e-b49f0f0859a5">DELEGATEITEMID</a> structures. It is the delegate's job to pack its data into the pointer to an item identifier list (PIDL) in the <b>DELEGATEITEMID</b> format.



