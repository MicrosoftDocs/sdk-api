---
UID: NN:wmsdkidl.IWMPropertyVault
title: IWMPropertyVault (wmsdkidl.h)
author: windows-sdk-content
description: The IWMPropertyVault interface provides methods to store and retrieve properties.
old-location: wmformat\iwmpropertyvault.htm
tech.root: wmformat
ms.assetid: 0e51a9be-afd4-430b-8339-f45e8f9a7d20
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPropertyVault, IWMPropertyVault interface [windows Media Format], IWMPropertyVault interface [windows Media Format],described, IWMPropertyVaultInterface, wmformat.iwmpropertyvault, wmsdkidl/IWMPropertyVault
ms.topic: interface
req.header: wmsdkidl.h
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
 - wmsdkidl.h
api_name:
 - IWMPropertyVault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPropertyVault interface


## -description



The <b>IWMPropertyVault</b> interface provides methods to store and retrieve properties. Currently, you can use this interface to set properties associated with variable bit rate (VBR) encoding. The generic nature of <b>IWMPropertyVault</b> allows for its use in other situations in future versions of the Format SDK.

<b>IWMPropertyVault</b> is exposed by stream configuration objects. To obtain a pointer to <b>IWMPropertyVault</b>, you must call the <b>QueryInterface</b> method of one of the other interfaces of an existing stream configuration object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPropertyVault</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPropertyVault</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPropertyVault</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757417(v=VS.85).aspx">Clear</a>
</td>
<td align="left" width="63%">
Removes all items from the property vault.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757418(v=VS.85).aspx">CopyPropertiesFrom</a>
</td>
<td align="left" width="63%">
Copies all of the properties from another property vault.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edecc6d2-f784-4205-bd79-6098e553d5cd">GetPropertyByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a property from the vault by its index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757420(v=VS.85).aspx">GetPropertyByName</a>
</td>
<td align="left" width="63%">
Retrieves a property from the vault by its name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757421(v=VS.85).aspx">GetPropertyCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of properties in the vault.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757422(v=VS.85).aspx">SetProperty</a>
</td>
<td align="left" width="63%">
Adds a property to the vault, or changes the value of an existing property.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757228(v=VS.85).aspx">IWMMediaProps</a>
</td>
<td>IID_IWMMediaProps</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798546(v=VS.85).aspx">IWMStreamConfig</a>
</td>
<td>IID_IWMStreamConfig</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798547(v=VS.85).aspx">IWMStreamConfig2</a>
</td>
<td>IID_IWMStreamConfig2</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798554(v=VS.85).aspx">IWMStreamConfig3</a>
</td>
<td>IID_IWMStreamConfig3</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd798711(v=VS.85).aspx">IWMVideoMediaProps</a> (on video streams only)</td>
<td>IID_IWMVideoMediaProps</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/228e334c-9d9b-4604-a225-73af7af3255f">Stream Configuration Object</a>
 

 

