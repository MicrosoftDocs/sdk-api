---
UID: NN:wbemcli.IWbemServices
title: IWbemServices (wbemcli.h)
author: windows-sdk-content
description: Used by clients and providers to access WMI services. The interface is implemented by WMI and WMI providers, and is the primary WMI interface.
old-location: wmi\iwbemservices.htm
tech.root: WmiSdk
ms.assetid: 58e2ecca-7d1f-4831-93fc-f946f8ada2c0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWbemServices, IWbemServices interface [Windows Management Instrumentation], IWbemServices interface [Windows Management Instrumentation],described, _hmm_iwbemservices, wbemcli/IWbemServices, wmi.iwbemservices
ms.topic: interface
f1_keywords: 
 - "wbemcli/IWbemServices"
dev_langs:
 - c++
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Esscli.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Ntevt.dll
 - Stdprov.dll
 - Viewprov.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wbemsvc.dll
 - Wmipicmp.dll
 - Wmidcprv.dll
 - Wmipjobj.dll
 - Wmiprvsd.dll
api_name:
 - IWbemServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemServices interface


## -description


The <b>IWbemServices</b> interface is used by clients and providers to access WMI services. The interface is implemented by WMI and WMI providers, and is the primary WMI interface.

```cpp
    IWbemClassObject *pObj = NULL;

    //The pWbemSvc pointer is of type IWbemServices*
    pWbemSvc->GetObject(L"path", 0, 0, &pObj, 0);
```



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-cancelasynccall">CancelAsyncCall</a>
</td>
<td align="left" width="63%">
Cancels a currently executing asynchronous call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenum">CreateClassEnum</a>
</td>
<td align="left" width="63%">
Creates a class enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync">CreateClassEnumAsync</a>
</td>
<td align="left" width="63%">
Creates a class enumerator that executes asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">CreateInstanceEnum</a>
</td>
<td align="left" width="63%">
Creates an instance enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync">CreateInstanceEnumAsync</a>
</td>
<td align="left" width="63%">
Creates an instance enumerator that executes asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclass">DeleteClass</a>
</td>
<td align="left" width="63%">
Deletes a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteclassasync">DeleteClassAsync</a>
</td>
<td align="left" width="63%">
Deletes a class and receives confirmation asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstance">DeleteInstance</a>
</td>
<td align="left" width="63%">
Deletes a specific instance of a class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync">DeleteInstanceAsync</a>
</td>
<td align="left" width="63%">
Deletes an instance and provides confirmation asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">ExecMethod</a>
</td>
<td align="left" width="63%">
Executes an object method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync">ExecMethodAsync</a>
</td>
<td align="left" width="63%">
Executes an object method asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationquery">ExecNotificationQuery</a>
</td>
<td align="left" width="63%">
Executes a query to receive events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync">ExecNotificationQueryAsync</a>
</td>
<td align="left" width="63%">
Executes a query to receive events asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">ExecQuery</a>
</td>
<td align="left" width="63%">
Executes a query to retrieve classes or instances.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync">ExecQueryAsync</a>
</td>
<td align="left" width="63%">
Executes a query to retrieve classes or instances asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an object—an instance or class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync">GetObjectAsync</a>
</td>
<td align="left" width="63%">
Asynchronously retrieves an object—an instance or class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-opennamespace">OpenNamespace</a>
</td>
<td align="left" width="63%">
Opens a specific child namespace for operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">PutClass</a>
</td>
<td align="left" width="63%">
Creates or updates a class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclassasync">PutClassAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates or updates a class definition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">PutInstance</a>
</td>
<td align="left" width="63%">
Creates or updates an instance of a specific class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync">PutInstanceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates or updates an instance of a specific class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-queryobjectsink">QueryObjectSink</a>
</td>
<td align="left" width="63%">
Allows a caller to obtain a notification handler sink.

</td>
</tr>
</table> 


## -remarks



Providers that implement the 
<b>IWbemServices</b> interface must follow the documented semantics of each method that they implement; and providers must support the specified error return codes. WMI implements all of the methods, and typically, each provider implements a small subset of the available functionality on the interface. Providers must return WBEM_E_PROVIDER_NOT_CAPABLE for any method that  they do not implement.

All outbound interface pointers from any 
<b>IWbemServices</b> method should be initialized to <b>NULL</b> before calling the interface method. For example, 
calls to the <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> method return an 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interface pointer that should be pre-initialized to <b>NULL</b> before the <b>IWbemServices::GetObject</b> method  call.


#### Examples

For multiple C++ examples that use IWbemServices, see the <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/wmi-c---application-examples">WMI C++ Application Examples</a> section.

The following code example shows how a provider can get an 
<b>IWbemServices</b> pointer. The code requires the following #include statements and references to compile.


```cpp
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```

```cpp
IWbemLocator *pIWbemLocator = NULL;

HRESULT hRes = CoCreateInstance (
            CLSID_WbemAdministrativeLocator,
            NULL ,
            CLSCTX_INPROC_SERVER | CLSCTX_LOCAL_SERVER , 
            IID_IUnknown ,
            ( void ** ) &pIWbemLocator
            ) ;

IWbemServices *pWbemServices = NULL;

if (SUCCEEDED(hRes))
{
    hRes = pIWbemLocator->ConnectServer(
                L"root\\CIMV2",  // Namespace
                NULL,          // Userid
                NULL,           // PW
                NULL,           // Locale
                0,              // flags
                NULL,           // Authority
                NULL,           // Context
                &pWbemServices
                );

pIWbemLocator->Release(); // Free memory resources.

// Use pWbemServices

}

// Clean up
pWbemServices->Release();
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/creating-wmi-providers">Creating WMI Providers</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/manipulating-class-and-instance-information">Manipulating Class and Instance Information</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/supplying-data-to-wmi-by-writing-a-provider">Supplying Data to WMI by Writing a Provider</a>
 

 

