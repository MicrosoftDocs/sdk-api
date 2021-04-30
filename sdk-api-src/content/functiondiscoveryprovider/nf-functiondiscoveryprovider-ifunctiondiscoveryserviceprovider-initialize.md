---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryServiceProvider.Initialize
title: IFunctionDiscoveryServiceProvider::Initialize (functiondiscoveryprovider.h)
description: Initializes an object that provides a specific interface that has been bound to the resource represented by the function instance.
helpviewer_keywords: ["IFunctionDiscoveryServiceProvider interface","Initialize method","IFunctionDiscoveryServiceProvider.Initialize","IFunctionDiscoveryServiceProvider::Initialize","Initialize","Initialize method","Initialize method","IFunctionDiscoveryServiceProvider interface","functiondiscoveryprovider/IFunctionDiscoveryServiceProvider::Initialize","ncd.ifunctiondiscoveryserviceprovider_initialize_method"]
old-location: ncd\ifunctiondiscoveryserviceprovider_initialize_method.htm
tech.root: ncd
ms.assetid: 339f6d42-20ea-4fd3-b03c-0cf34330baa0
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryServiceProvider interface,Initialize method, IFunctionDiscoveryServiceProvider.Initialize, IFunctionDiscoveryServiceProvider::Initialize, Initialize, Initialize method, Initialize method,IFunctionDiscoveryServiceProvider interface, functiondiscoveryprovider/IFunctionDiscoveryServiceProvider::Initialize, ncd.ifunctiondiscoveryserviceprovider_initialize_method
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionDiscoveryServiceProvider::Initialize
 - functiondiscoveryprovider/IFunctionDiscoveryServiceProvider::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryServiceProvider.Initialize
---

# IFunctionDiscoveryServiceProvider::Initialize


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Initializes an object that provides a specific interface that has been bound to the resource represented by the function instance.

## -parameters

### -param pIFunctionInstance [in]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface that represents the underlying resource.

### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the object.

### -param ppv [out]

The interface pointer requested in <i>riid</i>. Upon successful return, <i>*ppv</i> contains the requested interface pointer. Upon failure, <i>*ppv</i> contains <b>NULL</b>.

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

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryserviceprovider">IFunctionDiscoveryServiceProvider</a>