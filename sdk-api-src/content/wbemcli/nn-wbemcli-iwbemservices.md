---
UID: NN:wbemcli.IWbemServices
title: IWbemServices (wbemcli.h)
description: Used by clients and providers to access WMI services. The interface is implemented by WMI and WMI providers, and is the primary WMI interface.
helpviewer_keywords: ["IWbemServices","IWbemServices interface [Windows Management Instrumentation]","IWbemServices interface [Windows Management Instrumentation]","described","_hmm_iwbemservices","wbemcli/IWbemServices","wmi.iwbemservices"]
old-location: wmi\iwbemservices.htm
tech.root: wmi
ms.assetid: 58e2ecca-7d1f-4831-93fc-f946f8ada2c0
ms.date: 12/05/2018
ms.keywords: IWbemServices, IWbemServices interface [Windows Management Instrumentation], IWbemServices interface [Windows Management Instrumentation],described, _hmm_iwbemservices, wbemcli/IWbemServices, wmi.iwbemservices
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemServices
 - wbemcli/IWbemServices
dev_langs:
 - c++
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
---

# IWbemServices interface


## -description

The <b>IWbemServices</b> interface is used by clients and providers to access WMI services. The interface is implemented by WMI and WMI providers, and is the primary WMI interface.

```cpp
    IWbemClassObject *pObj = NULL;

    // The pWbemSvc pointer is of type IWbemServices*
    // BSTR is not compatible with wchar_t, need to allocate.
    BSTR path = SysAllocString(L"path");
    pWbemSvc->GetObject(path, 0, 0, &pObj, 0);
    SysFreeString(path);
```

## -inheritance

The <b>IWbemServices</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemServices</b> also has these types of members:

## -remarks

Providers that implement the 
<b>IWbemServices</b> interface must follow the documented semantics of each method that they implement; and providers must support the specified error return codes. WMI implements all of the methods, and typically, each provider implements a small subset of the available functionality on the interface. Providers must return WBEM_E_PROVIDER_NOT_CAPABLE for any method that  they do not implement.

All outbound interface pointers from any 
<b>IWbemServices</b> method should be initialized to <b>NULL</b> before calling the interface method. For example, 
calls to the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> method return an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> interface pointer that should be pre-initialized to <b>NULL</b> before the <b>IWbemServices::GetObject</b> method  call.


#### Examples

For multiple C++ examples that use IWbemServices, see the <a href="/windows/desktop/WmiSdk/wmi-c---application-examples">WMI C++ Application Examples</a> section.

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
    BSTR namespace = SysAllocString(L"root\\CIMV2");
    hRes = pIWbemLocator->ConnectServer(
                namespace,      // Namespace
                NULL,           // Userid
                NULL,           // PW
                NULL,           // Locale
                0,              // flags
                NULL,           // Authority
                NULL,           // Context
                &pWbemServices
                );
    SysFreeString(namespace);            

    pIWbemLocator->Release(); // Free memory resources.

    // Use pWbemServices

}

// Clean up
pWbemServices->Release();
```

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/WmiSdk/creating-wmi-providers">Creating WMI Providers</a>



<a href="/windows/desktop/WmiSdk/manipulating-class-and-instance-information">Manipulating Class and Instance Information</a>



<a href="/windows/desktop/WmiSdk/supplying-data-to-wmi-by-writing-a-provider">Supplying Data to WMI by Writing a Provider</a>
