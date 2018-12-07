---
UID: NN:comsvcs.IGetContextProperties
title: IGetContextProperties
author: windows-sdk-content
description: Enables the caller to obtain the properties associated with the current object's context.
old-location: cos\igetcontextproperties.htm
tech.root: cossdk
ms.assetid: 5e960c75-b074-4d4b-b5d6-252c26c70176
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IGetContextProperties, IGetContextProperties interface [COM+], IGetContextProperties interface [COM+],described, _cos_IGetContextProperties, comsvcs/IGetContextProperties, cos.igetcontextproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IGetContextProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGetContextProperties interface


## -description


Enables the caller to obtain the properties associated with the current object's context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetContextProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGetContextProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetContextProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/018b470e-726b-4777-8885-0ec7fa22f57a">Count</a>
</td>
<td align="left" width="63%">
Counts the number of context properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01ff9650-f7f1-440c-88d2-75ba793a2396">EnumNames</a>
</td>
<td align="left" width="63%">
Retrieves a list of the names of the current context properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/920938a9-44b1-4473-8204-1129b9599a72">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified context property.

</td>
</tr>
</table> 

