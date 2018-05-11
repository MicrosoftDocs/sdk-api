---
UID: NN:propsys.IPropertyDescriptionList
title: IPropertyDescriptionList
author: windows-driver-content
description: Exposes methods that extract information from a collection of property descriptions presented as a list.
old-location: properties\IPropertyDescriptionList.htm
old-project: properties
ms.assetid: e0530195-27da-4df7-884f-518e905f3c0e
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IPropertyDescriptionList, IPropertyDescriptionList interface [Windows Properties], IPropertyDescriptionList interface [Windows Properties],described, _shell_IPropertyDescriptionList, properties.IPropertyDescriptionList, propsys/IPropertyDescriptionList, shell.IPropertyDescriptionList
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
-	IPropertyDescriptionList
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0.6001 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyDescriptionList interface


## -description


Exposes methods that extract information from a collection of property descriptions presented as a list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyDescriptionList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyDescriptionList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyDescriptionList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a>
</td>
<td align="left" width="63%">
Gets the property description at the specified index in a property description list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of properties included in the property list.

</td>
</tr>
</table> 


## -remarks



Ordered lists of properties are used to select which properties are shown in various UI locations such as the details pane or an infotip.  The IPropertyDescriptionList interface provides access to the individual properties in such a list.  



To get an instance of the subsystem object that implements <a href="shell.IPropertyDescriptionList">IPropertyDescriptionList</a>, obtain an <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a> interface and call <a href="https://msdn.microsoft.com/443b95c9-0a9e-4ad5-8774-ad3b1b51c136">IShellItem2::GetPropertyDescriptionList</a>, or obtain the list in string form and call <a href="shell.PSGetPropertyDescriptionListFromString">PSGetPropertyDescriptionListFromString</a>. 

To obtain a property description list in string form, call <a href="https://msdn.microsoft.com/912b3653-340b-4186-b652-53d958534c1d">IShellItem2::GetString</a> with one of the PKEY_PropList keys.  For example, <code>PKEY_PropList_InfoTip</code> (<a href="shell.props_System_PropList_InfoTip">System.PropList.InfoTip</a>) will return the string form of a list of properties suitable for showing in an infotip.  If you are reading multiple values from an item, it is more efficient to call <a href="https://msdn.microsoft.com/library/windows/hardware/ff536962">IPropertyStore::GetValue</a> with a PKEY_PropList key so that the item is not reopened multiple times.  See Property Lists for details on how to register a property list string for a file type.




## -see-also




<a href="shell.PSGetPropertyDescriptionListFromString">PSGetPropertyDescriptionListFromString</a>
 

 

