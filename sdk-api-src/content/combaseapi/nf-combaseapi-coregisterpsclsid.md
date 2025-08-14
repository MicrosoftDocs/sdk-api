---
UID: NF:combaseapi.CoRegisterPSClsid
title: CoRegisterPSClsid function (combaseapi.h)
description: Enables a downloaded DLL to register its custom interfaces within its running process so that the marshaling code will be able to marshal those interfaces.
helpviewer_keywords: ["CoRegisterPSClsid","CoRegisterPSClsid function [COM]","_com_CoRegisterPSClsid","com.coregisterpsclsid","combaseapi/CoRegisterPSClsid"]
old-location: com\coregisterpsclsid.htm
tech.root: com
ms.assetid: a73dbd6d-d3f2-48d7-b053-b62f2f18f2d6
ms.date: 12/05/2018
ms.keywords: CoRegisterPSClsid, CoRegisterPSClsid function [COM], _com_CoRegisterPSClsid, com.coregisterpsclsid, combaseapi/CoRegisterPSClsid
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoRegisterPSClsid
 - combaseapi/CoRegisterPSClsid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoRegisterPSClsid
---

# CoRegisterPSClsid function


## -description

Enables a downloaded DLL to register its custom interfaces within its running process so that the marshaling code will be able to marshal those interfaces.

## -parameters

### -param riid [in]

A pointer to the IID of the interface to be registered.

### -param rclsid [in]

A pointer to the CLSID of the DLL that contains the proxy/stub code for the custom interface specified by <i>riid</i>.

## -returns

This function can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

Typically, the code responsible for marshaling an interface pointer into the current running process reads the <b>HKEY_CLASSES_ROOT\Interfaces</b> section of the registry to obtain the CLSID of the DLL containing the ProxyStub code to be loaded. To obtain the ProxyStub CLSIDs for an existing interface, the code calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetpsclsid">CoGetPSClsid</a> function.



In some cases, however, it may be desirable or necessary for an in-process handler or in-process server to make its custom interfaces available without writing to the registry. A DLL downloaded across a network may not even have permission to access the local registry, and because the code originated on another computer, the user, for security purposes, may want to run it in a restricted environment. Or a DLL may have custom interfaces that it uses to talk to a remote server and may also include the ProxyStub code for those interfaces. In such cases, a DLL needs an alternative way to register its interfaces. <b>CoRegisterPSClsid</b>, used in conjunction with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>, provides that alternative.


#### Examples

A DLL would typically call <b>CoRegisterPSClsid</b> as shown in the following code fragment.


```cpp
HRESULT RegisterMyCustomInterface(DWORD *pdwRegistrationKey)
{
    HRESULT hr = CoRegisterClassObject(CLSID_MyProxyStubClsid,
        pIPSFactoryBuffer,
        CLSCTX_INPROC_SERVER,
        REGCLS_MULTIPLEUSE
        pdwRegistrationKey);
    if(SUCCEEDED)(hr))
    {
        hr = CoRegisterPSClsid(IID_MyCustomInterface, CLSID_MyProxyStubClsid);
    }
 
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetpsclsid">CoGetPSClsid</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>