---
UID: NN:comsvcs.IContextProperties
title: IContextProperties
author: windows-sdk-content
description: Provides access to context object properties.
old-location: cos\icontextproperties.htm
tech.root: cossdk
ms.assetid: 95a5cfda-7587-496e-ba16-0dd2e8a4db32
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IContextProperties, IContextProperties interface [COM+], IContextProperties interface [COM+],described, _cos_IContextProperties, comsvcs/IContextProperties, cos.icontextproperties
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
 - IContextProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContextProperties interface


## -description


Provides access to context object properties. Each object context can have a user context property, which implements <b>IContextProperties</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContextProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContextProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96259fe8-138d-498e-8be0-1fe1cc3f0d83">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cae9eaf7-a422-4daa-9f0a-e7863f167112">EnumNames</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an enumerator for the context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc7748b4-5cf4-41c6-af7d-82b2478b084c">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a context object property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/112c9e08-de15-4e46-934a-5e57a1a52adc">RemoveProperty</a>
</td>
<td align="left" width="63%">
Removes a context object property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f6a27a2-37e9-4d4b-9d7e-916d791f03a5">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a context object property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a>
 

 

