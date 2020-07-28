---
UID: NF:strmif.IRegisterServiceProvider.RegisterService
title: IRegisterServiceProvider::RegisterService (strmif.h)
description: The RegisterService method registers an object as a service.
helpviewer_keywords: ["IRegisterServiceProvider interface [DirectShow]","RegisterService method","IRegisterServiceProvider.RegisterService","IRegisterServiceProvider::RegisterService","IRegisterServiceProviderRegisterService","RegisterService","RegisterService method [DirectShow]","RegisterService method [DirectShow]","IRegisterServiceProvider interface","dshow.iregisterserviceprovider_registerservice","strmif/IRegisterServiceProvider::RegisterService"]
old-location: dshow\iregisterserviceprovider_registerservice.htm
tech.root: dshow
ms.assetid: be8c3a89-687e-4a53-9fd0-0ec676e27ce0
ms.date: 12/05/2018
ms.keywords: IRegisterServiceProvider interface [DirectShow],RegisterService method, IRegisterServiceProvider.RegisterService, IRegisterServiceProvider::RegisterService, IRegisterServiceProviderRegisterService, RegisterService, RegisterService method [DirectShow], RegisterService method [DirectShow],IRegisterServiceProvider interface, dshow.iregisterserviceprovider_registerservice, strmif/IRegisterServiceProvider::RegisterService
f1_keywords:
- strmif/IRegisterServiceProvider.RegisterService
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IRegisterServiceProvider.RegisterService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegisterServiceProvider::RegisterService


## -description



The <code>RegisterService</code> method registers an object as a service.




## -parameters




### -param guidService [in]

Service identifier (SID) of the service.


### -param pUnkObject [in]

Pointer to the <b>IUnknown</b> interface of the service object, or <b>NULL</b> to unregister the service.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



A service is an interface that a client discovers through the COM <b>IServiceProvider::QueryService</b> method, instead of through the usual <b>IUnknown::QueryInterface</b> method. The difference between the two methods is that <b>QueryInterface</b> returns an interface on the original object, whereas <b>QueryService</b> may return an interface on another object. (More precisely, <b>QueryInterface</b> guarantees that you can query the original interface and the returned interface for <b>IUnknown</b>, and you will get back identical pointers. <b>QueryService</b> does not have this guarantee.)

The <code>RegisterService</code> method enables you to register a service with the Filter Graph Manager. Other objects can then use the <b>IServiceProvider</b> interface to retrieve your object. This facilitates communication between separate COM objects, using the Filter Graph Manager as the central communication point.

A service is identified by a GUID, called the service identifier (SID). One service can support multiple interfaces. To register the service, call <code>RegisterService</code>, as shown in the following code:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
DEFINE_GUID(SID_MyService, ....);
IRegisterServiceProvider *pRSP;
hr = pGraph-&gt;QueryInterface(IID_IRegisterServiceProvider, (void**)&amp;pRSP);
if (SUCCEEDED(hr))
{
    IUnknown pServiceObj;
    MyCreateServiceHelper(SID_MyService, &amp;pServiceObj);
    pRSP-&gt;RegisterService(SID_MyService, pServiceObj);
    pRSP-&gt;Release();
    pServiceObj-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
This example assumes that MyCreateServiceHelper is a helper function that creates the service object. A client could get a pointer to the service object by calling <b>IServiceProvider::QueryService</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IServiceProvider *pSP;
hr = pGraph-&gt;QueryInterface(IID_IServiceProvider, (void**)&amp;pSP);
if (SUCCEEDED(hr))
{
    ISomeInterface *pService;
    hr = pSP-&gt;QueryService(SID_MyService, IID_ISomeInterface, (void**)&amp;pService);
    pSP-&gt;Release();
    if (SUCCEEDED(hr))
    {
        pService-&gt;SomeMethod();
        pService-&gt;Release();
    }
};
</pre>
</td>
</tr>
</table></span></div>
To unregister the service, call <code>RegisterService</code> with a <b>NULL</b> pointer in the second parameter:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
pRSP-&gt;RegisterService(SID_MyService, NULL);
</pre>
</td>
</tr>
</table></span></div>
When the Filter Graph Manager is released, it unregisters all services.

The Filter Graph Manager keeps a reference count on the service object until the service is unregistered. To prevent circular reference counts, the service object should not hold a reference count on the Filter Graph Manager. For example, you cannot use the destructor method of the service object to unregister the service, because as long as the service holds a reference count on the Filter Graph Manager, the destructor will never be called. One solution is to create a separate object that registers and unregisters the service. Or, you can simply release the service object after you register it and let the Filter Graph Manager control its lifetime.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iregisterserviceprovider">IRegisterServiceProvider Interface</a>
 

 

