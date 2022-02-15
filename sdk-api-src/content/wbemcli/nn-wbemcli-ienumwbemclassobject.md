---
UID: NN:wbemcli.IEnumWbemClassObject
title: IEnumWbemClassObject (wbemcli.h)
description: The IEnumWbemClassObject interface is used to enumerate Common Information Model (CIM) objects and is similar to a standard COM enumerator.
helpviewer_keywords: ["IEnumWbemClassObject","IEnumWbemClassObject interface [Windows Management Instrumentation]","IEnumWbemClassObject interface [Windows Management Instrumentation]","described","_hmm_ienumwbemclassobject","wbemcli/IEnumWbemClassObject","wmi.ienumwbemclassobject"]
old-location: wmi\ienumwbemclassobject.htm
tech.root: wmi
ms.assetid: 142ea48d-d47b-4b7b-ab84-049a54955488
ms.date: 12/05/2018
ms.keywords: IEnumWbemClassObject, IEnumWbemClassObject interface [Windows Management Instrumentation], IEnumWbemClassObject interface [Windows Management Instrumentation],described, _hmm_ienumwbemclassobject, wbemcli/IEnumWbemClassObject, wmi.ienumwbemclassobject
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
req.dll: Fastprox.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumWbemClassObject
 - wbemcli/IEnumWbemClassObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IEnumWbemClassObject
---

# IEnumWbemClassObject interface


## -description

The 
<b>IEnumWbemClassObject</b> interface is used to enumerate <a href="/windows/desktop/WmiSdk/gloss-c">Common Information Model</a> (CIM) objects and is similar to a standard COM enumerator.

An object of type 
<b>IEnumWbemClassObject</b> is received from calls to the following methods:
<ul>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenum">IWbemServices::CreateClassEnum</a>
</li>
<li>
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationquery">IWbemServices::ExecNotificationQuery</a>
</li>
</ul>CIM objects are retrieved from an enumeration as objects of type 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> by calling the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-next">Next</a> method. You can reset an enumeration back to the beginning by calling the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-reset">Reset</a> method.

## -inheritance

The <b>IEnumWbemClassObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumWbemClassObject</b> also has these types of members:

## -remarks

<b>IEnumWbemClassObject</b> is the object returned from a WMI query, and is used to enumerate through the returned values. For more information on how to use this class, see <a href="/windows/desktop/WmiSdk/querying-wmi">Querying WMI</a> and <a href="/windows/desktop/WmiSdk/enumerating-wmi">Enumerating WMI</a>.


#### Examples

The following C++ code sample describes how to retrieve an <b>IEnumWbemClassObject</b>.


```cpp
void ExecQuerySync(IWbemServices *pSvc)
{
    // Query for all users and groups.

    BSTR Language = SysAllocString(L"WQL");
    BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

    // Initialize the IEnumWbemClassObject pointer.
    IEnumWbemClassObject *pEnum = 0;

    // Issue the query.
    HRESULT hRes = pSvc->ExecQuery(
        Language,
        Query,
        WBEM_FLAG_FORWARD_ONLY,         // Flags
        0,                              // Context
        &pEnum
        );

    SysFreeString(Query);
    SysFreeString(Language);

    if (hRes != 0)
    {
        printf("Error\n");
        return;
    }
    
    ULONG uTotal = 0;

    // Retrieve the objects in the result set.
    for (;;)
    {
        IWbemClassObject *pObj = 0;
        ULONG uReturned = 0;

        hRes = pEnum->Next(
            0,                  // Time out
            1,                  // One object
            &pObj,
            &uReturned
            );

        uTotal += uReturned;

        if (uReturned == 0)
            break;

        // Use the object.
        
        // ...
        
        // Release it.
        // ===========
        
        pObj->Release();    // Release objects not owned.            
    }

    // All done.
    pEnum->Release();
}

```

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for
    WMI</a>



<a href="/windows/desktop/WmiSdk/enumerating-wmi">Enumerating WMI</a>
