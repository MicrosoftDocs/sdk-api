---
UID: NF:functiondiscoveryprovider.IProviderProperties.GetValue
title: IProviderProperties::GetValue
author: windows-sdk-content
description: Gets the value of the specified property key.
old-location: ncd\iproviderproperties_getvalue_method.htm
old-project: fundisc
ms.assetid: c32a5367-ef39-4852-bf3b-203d27d0a2d0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetValue, GetValue method, GetValue method,IProviderProperties interface, IProviderProperties interface,GetValue method, IProviderProperties.GetValue, IProviderProperties::GetValue, functiondiscoveryprovider/IProviderProperties::GetValue, ncd.iproviderproperties_getvalue_method
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
 - IProviderProperties.GetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IProviderProperties::GetValue


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the value of the specified property key.


## -parameters




### -param pIFunctionInstance [in]

An <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface pointer.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


### -param Key [in]

The property key reference.


### -param ppropVar [out]

The value of the property key specified by <i>Key</i>. The <b>PROPVARIANT</b> type is VT_EMPTY if the key is not found in the property store.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains an invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppropVar</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate enough memory to perform the operation.

</td>
</tr>
</table>
 




## -remarks



To change the value of a property key, use the <a href="https://msdn.microsoft.com/5aa3e6a3-febc-4d2d-b58b-abfad28d325d">SetValue</a> method.

If a value for <i>Key</i> could not be found, the return value will be <b>S_OK</b> and <i>ppropVar</i> will be set to <b>VT_NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/d6d3d1d1-d2fb-409c-be37-3cd286e325a3">IProviderProperties</a>
 

 

