---
UID: NN:propsys.IPropertyStoreFactory
title: IPropertyStoreFactory
author: windows-driver-content
description: Exposes methods to get an IPropertyStore object.
old-location: properties\IPropertyStoreFactory.htm
old-project: properties
ms.assetid: 78ea822d-da8e-4883-b0eb-4277e7eb87a2
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IPropertyStoreFactory, IPropertyStoreFactory interface [Windows Properties], IPropertyStoreFactory interface [Windows Properties], described, _shell_IPropertyStoreFactory, properties.IPropertyStoreFactory, propsys/IPropertyStoreFactory, shell.IPropertyStoreFactory
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyStoreFactory
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyStoreFactory interface


## -description


Exposes methods to get an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStoreFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyStoreFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyStoreFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyStoreFactory_GetPropertyStore">GetPropertyStore</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object that corresponds to the supplied flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="shell.IPropertyStoreFactory_GetPropertyStoreForKeys">GetPropertyStoreForKeys</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a> object, given a set of property keys. This provides an alternative, possibly faster, method of getting an <b>IPropertyStore</b> object compared to calling <a href="shell.IPropertyStoreFactory_GetPropertyStore">IPropertyStoreFactory::GetPropertyStore</a>.

</td>
</tr>
</table> 


## -remarks




              This interface is typically obtained through <a href="https://msdn.microsoft.com/5e699494-1974-4b9b-8324-9394f7b96fe4">IShellFolder::BindToObject</a> or <a href="https://msdn.microsoft.com/fadd70cd-5018-4b71-af7b-d9c780ebddc5">IShellItem::BindToHandler</a>. It is useful for data source implementers who want to avoid the additional overhead of creating a property store through <a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a>. However, <b>IShellItem2::GetPropertyStore</b> is the recommended method to obtain a property store unless you are implementing a data source through a Shell folder extension.
            




## -see-also




<a href="shell.PSCreatePropertyStoreFromObject">PSCreatePropertyStoreFromObject</a>
 

 

