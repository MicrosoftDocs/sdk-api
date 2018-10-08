---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstanceReleased
title: IFunctionDiscoveryProvider::InstanceReleased
author: windows-sdk-content
description: Releases the specified function instance and frees the memory previously allocated.
old-location: ncd\ifunctiondiscoveryprovider_instancereleased.htm
tech.root: fundisc
ms.assetid: fa348767-8a83-4a45-9411-1e9eb545d97d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstanceReleased method, IFunctionDiscoveryProvider.InstanceReleased, IFunctionDiscoveryProvider::InstanceReleased, InstanceReleased, InstanceReleased method, InstanceReleased method,IFunctionDiscoveryProvider interface, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstanceReleased, ncd.ifunctiondiscoveryprovider_instancereleased
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFunctionDiscoveryProvider.InstanceReleased
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProvider::InstanceReleased


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Releases the specified function instance and frees the memory previously allocated.


## -parameters




### -param pIFunctionInstance [in]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface.


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




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 

