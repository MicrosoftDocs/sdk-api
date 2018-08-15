---
UID: NF:functiondiscoveryprovider.IProviderProperties.SetValue
title: IProviderProperties::SetValue
author: windows-sdk-content
description: Sets the value of the specified property key.
old-location: ncd\iproviderproperties_setvalue.htm
old-project: fundisc
ms.assetid: 5aa3e6a3-febc-4d2d-b58b-abfad28d325d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IProviderProperties interface,SetValue method, IProviderProperties.SetValue, IProviderProperties::SetValue, SetValue, SetValue method, SetValue method,IProviderProperties interface, functiondiscoveryprovider/IProviderProperties::SetValue, ncd.iproviderproperties_setvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PropertyConstraint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IProviderProperties.SetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IProviderProperties::SetValue


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets the value of the specified property key.


## -parameters




### -param pIFunctionInstance [in]

An <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


### -param Key [in]

The property key for the property to be set.


### -param ppropVar [in]

The property data. To remove the property from the store, specify a <b>PROPVARIANT</b> with the type VT_EMPTY.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pIFunctionInstance</i>, <i>pvProviderInstanceContext</i>, or <i>ppropVar</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d6d3d1d1-d2fb-409c-be37-3cd286e325a3">IProviderProperties</a>
 

 

