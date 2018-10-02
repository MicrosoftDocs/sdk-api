---
UID: NN:xamlom.IVisualTreeService3
title: IVisualTreeService3
author: windows-sdk-content
description: Represents additional capabilities of an IVisualTreeService2 object.
old-location: xaml_diagnostics\ivisualtreeservice3.htm
tech.root: xaml_diagnostics
ms.assetid: 20AD2DC4-388E-458E-AA44-8B2F3464FD6C
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVisualTreeService3, IVisualTreeService3 interface, IVisualTreeService3 interface,described, xaml_diagnostics.ivisualtreeservice3, xamlom/IVisualTreeService3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
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
 - xamlom.h
api_name:
 - IVisualTreeService3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVisualTreeService3 interface


## -description


Represents additional capabilities of an <a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService2</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVisualTreeService3</b> interface inherits from <a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService2</a>. <b>IVisualTreeService3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVisualTreeService3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86590A71-8BFC-4214-9F7C-1DF5B8391552">AddDictionaryItem</a>
</td>
<td align="left" width="63%">
	Adds an item to a <a href="https://msdn.microsoft.com/cb82a1f5-ebcf-4ffd-842b-78313e5eff9c">ResourceDictionary</a>, and re-resolves all elements in the tree that reference a resource with the specified key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E836FE12-A49A-427C-8013-F1AFBD2C08A2">GetDictionaryItem</a>
</td>
<td align="left" width="63%">
Gets an item from a <a href="https://msdn.microsoft.com/cb82a1f5-ebcf-4ffd-842b-78313e5eff9c">ResourceDictionary</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6239D855-7408-47ED-9090-E7726E7E403E">RemoveDictionaryItem</a>
</td>
<td align="left" width="63%">
	Removes an item from a <a href="https://msdn.microsoft.com/cb82a1f5-ebcf-4ffd-842b-78313e5eff9c">ResourceDictionary</a>, and re-resolves all elements in the tree that reference a resource with the specified key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DDF1FD0-AD9B-4679-831D-CEDF6524181B">ResolveResource</a>
</td>
<td align="left" width="63%">
Resolves a resource for an element in the tree and applies the resource to the property provided by the specified property index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5C0896E4-E37E-49DF-B303-1814BCA6F5B3">IVisualTreeService2</a>
 

 

