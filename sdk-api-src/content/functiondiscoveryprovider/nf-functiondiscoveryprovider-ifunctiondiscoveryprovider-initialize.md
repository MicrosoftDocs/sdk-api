---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.Initialize
title: IFunctionDiscoveryProvider::Initialize (functiondiscoveryprovider.h)
description: Initializes the Function Discovery provider object.
helpviewer_keywords: ["IFunctionDiscoveryProvider interface","Initialize method","IFunctionDiscoveryProvider.Initialize","IFunctionDiscoveryProvider::Initialize","Initialize","Initialize method","Initialize method","IFunctionDiscoveryProvider interface","STGM_READ","STGM_READWRITE","STGM_WRITE","functiondiscoveryprovider/IFunctionDiscoveryProvider::Initialize","ncd.ifunctiondiscoveryprovider_initialize_method"]
old-location: ncd\ifunctiondiscoveryprovider_initialize_method.htm
tech.root: ncd
ms.assetid: 084d6d91-4637-4325-887b-e9f46ecaaee4
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,Initialize method, IFunctionDiscoveryProvider.Initialize, IFunctionDiscoveryProvider::Initialize, Initialize, Initialize method, Initialize method,IFunctionDiscoveryProvider interface, STGM_READ, STGM_READWRITE, STGM_WRITE, functiondiscoveryprovider/IFunctionDiscoveryProvider::Initialize, ncd.ifunctiondiscoveryprovider_initialize_method
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
 - IFunctionDiscoveryProvider::Initialize
 - functiondiscoveryprovider/IFunctionDiscoveryProvider::Initialize
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
 - IFunctionDiscoveryProvider.Initialize
---

# IFunctionDiscoveryProvider::Initialize


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Initializes the Function Discovery provider object.  This method is intended to be called immediately after the object is created.

## -parameters

### -param pIFunctionDiscoveryProviderFactory [in]

A pointer to the <a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryproviderfactory">IFunctionDiscoveryProviderFactory</a> interface. The provider should use this interface to create new Function Discovery objects.

### -param pIFunctionDiscoveryNotification [in]

A pointer to an <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctiondiscoverynotification">IFunctionDiscoveryNotification</a> interface. The provider should use this interface to send <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onupdate">OnUpdate</a>, <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onevent">OnEvent</a>, and <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctiondiscoverynotification-onerror">OnError</a> notifications to the Function Discovery notification queue. Queued notifications are sent to client programs by Function Discovery.

### -param lcidUserDefault [in]

The locale identifier of the caller. The provider should use <i>lcidUserDefault</i> to return localized strings for the resource enumerated by the provider.

### -param pdwStgAccessCapabilities [out]

Specifies the least restrictive possible access mode of the  property stores associated with the function instances created by this provider.  

If the DWORD value is set to -1, <a href="/windows/desktop/api/functiondiscoveryprovider/nf-functiondiscoveryprovider-ifunctiondiscoveryprovider-instancepropertystorevalidateaccess">InstancePropertyStoreValidateAccess</a> will be called every time <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstance-openpropertystore">OpenPropertyStore</a> is called on a function instance created by this provider.  Otherwise, the value specified by this parameter determines the least restrictive possible access mode for all property stores associated with all function instances created by this provider. A more restrictive access mode will be applied to an individual property store if a client calls <b>OpenPropertyStore</b> with the <i>dwStgAccess</i> parameter set to a value that is more restrictive than the specified  <i>pdwStgAccessCapabilities</i> value.

For efficiency, specify a <i>pdwStgAccessCapabilities</i>  value whenever possible.

The following modes are supported: 

<a id="STGM_READ"></a>
<a id="stgm_read"></a>


#### STGM_READ

<a id="STGM_READWRITE"></a>
<a id="stgm_readwrite"></a>


#### STGM_READWRITE

<a id="STGM_WRITE"></a>
<a id="stgm_write"></a>


#### STGM_WRITE

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

If your provider is going to create Function Discovery objects, queue notifications, or enumerate resources with localized strings, you must call <b>AddRef</b> on and cache  the initialized <i>pIFunctionDiscoveryProviderFactory</i>, <i>pIFunctionDiscoveryNotification</i>, and <i>lcidUserDefault</i> parameters for later use when you implement the <b>Initialize</b> method.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>