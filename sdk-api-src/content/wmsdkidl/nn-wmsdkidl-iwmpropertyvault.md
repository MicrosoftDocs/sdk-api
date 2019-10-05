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
f1_keywords: 
 - "wmsdkidl/IWMPropertyVault"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPropertyVault interface


## -description



The <b>IWMPropertyVault</b> interface provides methods to store and retrieve properties. Currently, you can use this interface to set properties associated with variable bit rate (VBR) encoding. The generic nature of <b>IWMPropertyVault</b> allows for its use in other situations in future versions of the Format SDK.

<b>IWMPropertyVault</b> is exposed by stream configuration objects. To obtain a pointer to <b>IWMPropertyVault</b>, you must call the <b>QueryInterface</b> method of one of the other interfaces of an existing stream configuration object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPropertyVault</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPropertyVault</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all items from the property vault.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-copypropertiesfrom">CopyPropertiesFrom</a>
</td>
<td align="left" width="63%">
Copies all of the properties from another property vault.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyindex">GetPropertyByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a property from the vault by its index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname">GetPropertyByName</a>
</td>
<td align="left" width="63%">
Retrieves a property from the vault by its name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertycount">GetPropertyCount</a>
</td>
<td align="left" width="63%">
Retrieves the total number of properties in the vault.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty">SetProperty</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops">IWMMediaProps</a>
</td>
<td>IID_IWMMediaProps</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a>
</td>
<td>IID_IWMStreamConfig</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2</a>
</td>
<td>IID_IWMStreamConfig2</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3">IWMStreamConfig3</a>
</td>
<td>IID_IWMStreamConfig3</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps</a> (on video streams only)</td>
<td>IID_IWMVideoMediaProps</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/stream-configuration-object">Stream Configuration Object</a>
 

 

