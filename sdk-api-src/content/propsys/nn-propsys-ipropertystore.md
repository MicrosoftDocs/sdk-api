---
UID: NN:propsys.IPropertyStore
title: IPropertyStore
author: windows-driver-content
description: This interface exposes methods used to enumerate and manipulate property values.
old-location: audio\ipropertystore.htm
old-project: audio
ms.assetid: 63afd5b1-87cc-4e0a-8964-2138c5fbff46
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IPropertyStore, IPropertyStore interface [Audio Devices], IPropertyStore interface [Audio Devices], described, audio.ipropertystore, audio_syseffects_r_1efc1bca-70e7-4db2-aea3-4c1d4aa1a39a.xml, propsys/IPropertyStore
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyStore
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536957">IPropertyStore::Commit</a>
</td>
<td align="left" width="63%">
After a change has been made, this method saves the changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536959">IPropertyStore::GetAt</a>
</td>
<td align="left" width="63%">
Gets a property key from the property array of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536960">IPropertyStore::GetCount</a>
</td>
<td align="left" width="63%">
This method returns a count of the number of properties that are attached to the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a>
</td>
<td align="left" width="63%">
This method retrieves the data for a specific property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536963">IPropertyStore::SetValue</a>
</td>
<td align="left" width="63%">
This method sets a property value or replaces or removes an existing value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/jj151546">APOInitSystemEffects</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj151547">AudioFXExtensionParams</a>
 

 

