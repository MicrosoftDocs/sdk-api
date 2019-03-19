---
UID: NN:propsys.IPropertyStoreCache
title: IPropertyStoreCache (propsys.h)
author: windows-sdk-content
description: Exposes methods that allow a handler to manage various states for each property.
old-location: properties\IPropertyStoreCache.htm
tech.root: properties
ms.assetid: ac4f7e3b-6702-4239-b248-0645d961fbf8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPropertyStoreCache, IPropertyStoreCache interface [Windows Properties], IPropertyStoreCache interface [Windows Properties],described, properties.IPropertyStoreCache, propsys/IPropertyStoreCache, shell.IPropertyStoreCache, shell_IPropertyStoreCache
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
 - IPropertyStoreCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyStoreCache interface


## -description


Exposes methods that allow a handler to manage various states for each property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStoreCache</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a>. <b>IPropertyStoreCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyStoreCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms710659(v=VS.85).aspx">GetState</a>
</td>
<td align="left" width="63%">
Gets the state of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761465(v=VS.85).aspx">GetValueAndState</a>
</td>
<td align="left" width="63%">
Gets value and state data for a property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd375990(v=VS.85).aspx">SetState</a>
</td>
<td align="left" width="63%">
Sets the property state of a specified property key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761469(v=VS.85).aspx">SetValueAndState</a>
</td>
<td align="left" width="63%">
Sets value and state data for a property key.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided by CLSID_InMemoryPropertyStore. Users should never need to implement it themselves.

                

CLSID_InMemoryPropertyStore implements <a href="https://msdn.microsoft.com/en-us/library/Bb761466(v=VS.85).aspx">IPropertyStoreCache</a> instead of <a href="https://msdn.microsoft.com/en-us/library/Bb761474(v=VS.85).aspx">IPropertyStore</a> so that it can store additional state information (<a href="https://msdn.microsoft.com/en-us/library/Bb762531(v=VS.85).aspx">PSC_STATE</a>) about each of the properties in the cache. This information can be useful for property handler implementers. It can also be useful in other scenarios where a cache of property values is needed.



