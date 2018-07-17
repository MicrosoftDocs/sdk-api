---
UID: NN:shobjidl_core.IEnumAssocHandlers
title: IEnumAssocHandlers
author: windows-sdk-content
description: Exposes a method that allows enumeration of a collection of handlers associated with particular file name extensions.
old-location: shell\IEnumAssocHandlers.htm
old-project: shell
ms.assetid: c8b11157-4d00-4ab1-aea5-ce8ae35c43ce
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IEnumAssocHandlers, IEnumAssocHandlers interface [Windows Shell], IEnumAssocHandlers interface [Windows Shell],described, _shell_IEnumAssocHandlers, shell.IEnumAssocHandlers, shobjidl_core/IEnumAssocHandlers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IEnumAssocHandlers
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IEnumAssocHandlers interface


## -description


Exposes a method that allows enumeration of a collection of handlers associated with particular file name extensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAssocHandlers</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumAssocHandlers</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAssocHandlers</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of elements.

</td>
</tr>
</table> 


## -remarks




<a href="https://msdn.microsoft.com/83db466b-e00c-4015-879f-c5c222f45b8c">SHAssocEnumHandlers</a> is the usual method of creating an IEnumAssocHandlers pointer.




## -see-also




<a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a>



<a href="https://msdn.microsoft.com/b602280e-4237-4539-9a10-cec21c65e90d">IAssocHandlerInvoker</a>



<a href="https://msdn.microsoft.com/83db466b-e00c-4015-879f-c5c222f45b8c">SHAssocEnumHandlers</a>
 

 

