---
UID: NF:functiondiscoveryprovider.IProviderProperties.GetCount
title: IProviderProperties::GetCount (functiondiscoveryprovider.h)
author: windows-sdk-content
description: Gets the number of properties in the property store.
old-location: ncd\iproviderproperties_getcount_method.htm
tech.root: FunDisc
ms.assetid: 25ed5782-c19e-4c3d-81f1-74e0ea3e195e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method, GetCount method,IProviderProperties interface, IProviderProperties interface,GetCount method, IProviderProperties.GetCount, IProviderProperties::GetCount, functiondiscoveryprovider/IProviderProperties::GetCount, ncd.iproviderproperties_getcount_method
ms.topic: method
req.header: functiondiscoveryprovider.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IProviderProperties.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProviderProperties::GetCount


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the number of properties in the property store.


## -parameters




### -param pIFunctionInstance [in]

An <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface pointer.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


### -param pdwCount [out]

The number of properties in the property store.


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
<i>pdwCount</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d6d3d1d1-d2fb-409c-be37-3cd286e325a3">IProviderProperties</a>
 

 

