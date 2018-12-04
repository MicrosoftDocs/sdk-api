---
UID: NN:propsys.IPropertyStore
title: IPropertyStore
author: windows-sdk-content
description: This interface exposes methods used to enumerate and manipulate property values.
old-location: audio\ipropertystore.htm
tech.root: audio
ms.assetid: 63afd5b1-87cc-4e0a-8964-2138c5fbff46
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IPropertyStore, IPropertyStore interface [Audio Devices], IPropertyStore interface [Audio Devices],described, audio.ipropertystore, audio_syseffects_r_1efc1bca-70e7-4db2-aea3-4c1d4aa1a39a.xml, propsys/IPropertyStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - Propsys.h
api_name:
 - IPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyStore interface


## -description


This interface exposes methods used to enumerate and manipulate property values. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3cc6815-a16f-45e7-a2d5-8f354f712170">IPropertyStore::Commit</a>
</td>
<td align="left" width="63%">
After a change has been made, this method saves the changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f93949a-d5d5-4fbf-8538-6171861e5884">IPropertyStore::GetAt</a>
</td>
<td align="left" width="63%">
Gets a property key from the property array of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23f7b982-29db-4960-9a1d-2f9e033ebf61">IPropertyStore::GetCount</a>
</td>
<td align="left" width="63%">
This method returns a count of the number of properties that are attached to the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11204335-0f00-4af8-8787-93e91248e5bd">IPropertyStore::GetValue</a>
</td>
<td align="left" width="63%">
This method retrieves the data for a specific property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be21bcb2-6875-4559-abd7-a496f0fcddd6">IPropertyStore::SetValue</a>
</td>
<td align="left" width="63%">
This method sets a property value or replaces or removes an existing value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/E33B1F94-4E3A-4EC1-AFB5-FD803FA391BC">APOInitSystemEffects</a>



<a href="https://msdn.microsoft.com/832F1190-ED3E-4059-AB45-18C23D98663B">AudioFXExtensionParams</a>
 

 

