---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryServiceProvider.Initialize
title: IFunctionDiscoveryServiceProvider::Initialize
author: windows-sdk-content
description: Initializes an object that provides a specific interface that has been bound to the resource represented by the function instance.
old-location: ncd\ifunctiondiscoveryserviceprovider_initialize_method.htm
old-project: FunDisc
ms.assetid: 339f6d42-20ea-4fd3-b03c-0cf34330baa0
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IFunctionDiscoveryServiceProvider interface,Initialize method, IFunctionDiscoveryServiceProvider.Initialize, IFunctionDiscoveryServiceProvider::Initialize, Initialize, Initialize method, Initialize method,IFunctionDiscoveryServiceProvider interface, functiondiscoveryprovider/IFunctionDiscoveryServiceProvider::Initialize, ncd.ifunctiondiscoveryserviceprovider_initialize_method
ms.prod: windows
ms.technology: windows-sdk
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
 - IFunctionDiscoveryServiceProvider.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFunctionDiscoveryServiceProvider::Initialize


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Initializes an object that provides a specific interface that has been bound to the resource represented by the function instance.


## -parameters




### -param pIFunctionInstance




### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the object.


### -param ppv [out]

The interface pointer requested in <i>riid</i>. Upon successful return, <i>*ppv</i> contains the requested interface pointer. Upon failure, <i>*ppv</i> contains <b>NULL</b>.


#### - pFunctionInstance [in]

A pointer to an <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface that represents the underlying resource.


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
</table>
 




## -remarks



Any error code indicates failure. The provider should return an appropriate error code if it is unable to create the desired object.




## -see-also




<a href="https://msdn.microsoft.com/dbdf27dc-5fb9-49ef-9a9b-ffcd7b148479">IFunctionDiscoveryServiceProvider</a>
 

 

