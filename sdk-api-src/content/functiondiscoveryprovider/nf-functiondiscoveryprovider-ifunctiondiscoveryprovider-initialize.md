---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.Initialize
title: IFunctionDiscoveryProvider::Initialize
author: windows-sdk-content
description: Initializes the Function Discovery provider object.
old-location: ncd\ifunctiondiscoveryprovider_initialize_method.htm
tech.root: fundisc
ms.assetid: 084d6d91-4637-4325-887b-e9f46ecaaee4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFunctionDiscoveryProvider interface,Initialize method, IFunctionDiscoveryProvider.Initialize, IFunctionDiscoveryProvider::Initialize, Initialize, Initialize method, Initialize method,IFunctionDiscoveryProvider interface, STGM_READ, STGM_READWRITE, STGM_WRITE, functiondiscoveryprovider/IFunctionDiscoveryProvider::Initialize, ncd.ifunctiondiscoveryprovider_initialize_method
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
 - IFunctionDiscoveryProvider.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFunctionDiscoveryProvider::Initialize


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Initializes the Function Discovery provider object.  This method is intended to be called immediately after the object is created.


## -parameters




### -param pIFunctionDiscoveryProviderFactory [in]

A pointer to the <a href="https://msdn.microsoft.com/576db617-0bca-4b46-839b-0f133f28cacb">IFunctionDiscoveryProviderFactory</a> interface. The provider should use this interface to create new Function Discovery objects.


### -param pIFunctionDiscoveryNotification [in]

A pointer to an <a href="https://msdn.microsoft.com/1819fe08-b151-482d-8e2c-1d599fd15609">IFunctionDiscoveryNotification</a> interface. The provider should use this interface to send <a href="https://msdn.microsoft.com/ab4d0fc6-de3f-49cf-b53c-573222a8bc89">OnUpdate</a>, <a href="https://msdn.microsoft.com/4ebfdf15-ca37-4905-b842-8854a0bd276b">OnEvent</a>, and <a href="https://msdn.microsoft.com/c4dcc4e9-7acf-44d3-b337-1ac01afa19b0">OnError</a> notifications to the Function Discovery notification queue. Queued notifications are sent to client programs by Function Discovery.


### -param lcidUserDefault [in]

The locale identifier of the caller. The provider should use <i>lcidUserDefault</i> to return localized strings for the resource enumerated by the provider. 


### -param pdwStgAccessCapabilities [out]

Specifies the least restrictive possible access mode of the  property stores associated with the function instances created by this provider.  

If the DWORD value is set to -1, <a href="https://msdn.microsoft.com/0ee8d65d-0be3-4171-946a-10a15b8f8eb7">InstancePropertyStoreValidateAccess</a> will be called every time <a href="https://msdn.microsoft.com/3e03567b-7bac-4bef-ae62-a040f0c33cfb">OpenPropertyStore</a> is called on a function instance created by this provider.  Otherwise, the value specified by this parameter determines the least restrictive possible access mode for all property stores associated with all function insteances created by this provider. A more restrictive access mode will be applied to an individual property store if a client calls <b>OpenPropertyStore</b> with the <i>dwStgAccess</i> parameter set to a value that is more restrictive than the specified  <i>pdwStgAccessCapabilities</i> value.

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




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 

