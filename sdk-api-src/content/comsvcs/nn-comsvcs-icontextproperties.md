---
UID: NN:comsvcs.IContextProperties
title: IContextProperties
author: windows-sdk-content
description: Provides access to context object properties.
old-location: cos\icontextproperties.htm
tech.root: cossdk
ms.assetid: 95a5cfda-7587-496e-ba16-0dd2e8a4db32
ms.author: windowssdkdev
ms.date: 12/5/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContextProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IContextProperties</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms684282(v=VS.85).aspx">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686468(v=VS.85).aspx">EnumNames</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an enumerator for the context object properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686992(v=VS.85).aspx">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a context object property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678952(v=VS.85).aspx">RemoveProperty</a>
</td>
<td align="left" width="63%">
Removes a context object property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681272(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a context object property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms685055(v=VS.85).aspx">IEnumNames</a>
 

 

