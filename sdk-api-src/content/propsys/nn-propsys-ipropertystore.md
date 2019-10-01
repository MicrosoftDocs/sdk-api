---
UID: NN:propsys.IPropertyStore
title: IPropertyStore (propsys.h)
author: windows-sdk-content
description: This interface exposes methods used to enumerate and manipulate property values.
old-location: audio\ipropertystore.htm
tech.root: audio
ms.assetid: 63afd5b1-87cc-4e0a-8964-2138c5fbff46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyStore, IPropertyStore interface [Audio Devices], IPropertyStore interface [Audio Devices],described, audio.ipropertystore, audio_syseffects_r_1efc1bca-70e7-4db2-aea3-4c1d4aa1a39a.xml, propsys/IPropertyStore
ms.topic: interface
f1_keywords: 
 - "propsys/IPropertyStore"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStore interface


## -description


This interface exposes methods used to enumerate and manipulate property values. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStore</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyStore</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-commit">IPropertyStore::Commit</a>
</td>
<td align="left" width="63%">
After a change has been made, this method saves the changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-getat">IPropertyStore::GetAt</a>
</td>
<td align="left" width="63%">
Gets a property key from the property array of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-getcount">IPropertyStore::GetCount</a>
</td>
<td align="left" width="63%">
This method returns a count of the number of properties that are attached to the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-getvalue">IPropertyStore::GetValue</a>
</td>
<td align="left" width="63%">
This method retrieves the data for a specific property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nf-propsys-ipropertystore-setvalue">IPropertyStore::SetValue</a>
</td>
<td align="left" width="63%">
This method sets a property value or replaces or removes an existing value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/audioenginebaseapo/ns-audioenginebaseapo-apoinitsystemeffects">APOInitSystemEffects</a>



<a href="https://docs.microsoft.com/windows/win32/api/audioenginebaseapo/ns-audioenginebaseapo-audiofxextensionparams">AudioFXExtensionParams</a>
 

 

