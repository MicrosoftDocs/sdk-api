---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstanceReleased
title: IFunctionDiscoveryProvider::InstanceReleased (functiondiscoveryprovider.h)
author: windows-sdk-content
description: Releases the specified function instance and frees the memory previously allocated.
old-location: ncd\ifunctiondiscoveryprovider_instancereleased.htm
tech.root: FunDisc
ms.assetid: fa348767-8a83-4a45-9411-1e9eb545d97d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstanceReleased method, IFunctionDiscoveryProvider.InstanceReleased, IFunctionDiscoveryProvider::InstanceReleased, InstanceReleased, InstanceReleased method, InstanceReleased method,IFunctionDiscoveryProvider interface, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstanceReleased, ncd.ifunctiondiscoveryprovider_instancereleased
ms.topic: method
f1_keywords: 
 - "functiondiscoveryprovider/IFunctionDiscoveryProvider.InstanceReleased"
dev_langs:
 - c++
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
 - IFunctionDiscoveryProvider.InstanceReleased
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFunctionDiscoveryProvider::InstanceReleased


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Releases the specified function instance and frees the memory previously allocated.


## -parameters




### -param pIFunctionInstance [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


## -returns



This method can return one of these values.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
</table>
 




## -remarks



When you implement this method, you must clean up the memory allocated for <i>ppvProviderInstanceContext</i> as necessary.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>
 

 

