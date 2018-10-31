---
UID: NN:propsys.INamedPropertyStore
title: INamedPropertyStore
author: windows-sdk-content
description: Exposes methods that get and set named properties.
old-location: shell\INamedPropertyStore.htm
tech.root: shell
ms.assetid: 5f7997ba-a5c8-42b5-90c8-5cb34afd6092
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: INamedPropertyStore, INamedPropertyStore interface [Windows Shell], INamedPropertyStore interface [Windows Shell],described, _shell_INamedPropertyStore, propsys/INamedPropertyStore, shell.INamedPropertyStore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - Propsys.h
api_name:
 - INamedPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INamedPropertyStore interface


## -description


Exposes methods that get and set named properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INamedPropertyStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INamedPropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INamedPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fd3896e-b170-49af-811e-a1f2facc7a84">GetNameAt</a>
</td>
<td align="left" width="63%">
Gets the name of a property at a specified index in the property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74bba1bf-e003-40bb-9118-4d647f78e409">GetNameCount</a>
</td>
<td align="left" width="63%">
Gets the number of property names in the property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d62fcacd-7af5-4618-9b76-bebb001bb827">GetNamedValue</a>
</td>
<td align="left" width="63%">
Gets the value of a named property from the named property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1ccf53f-3117-45c2-a0ff-94f1bb084414">SetNamedValue</a>
</td>
<td align="left" width="63%">
Sets the value of a named property.

</td>
</tr>
</table> 

