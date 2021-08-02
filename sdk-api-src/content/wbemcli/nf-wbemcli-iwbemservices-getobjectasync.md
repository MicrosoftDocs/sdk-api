---
UID: NF:wbemcli.IWbemServices.GetObjectAsync
title: IWbemServices::GetObjectAsync (wbemcli.h)
description: The IWbemServices::GetObjectAsync method retrieves an object, either a class definition or instance, based on its path.
helpviewer_keywords: ["GetObjectAsync","GetObjectAsync method [Windows Management Instrumentation]","GetObjectAsync method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","GetObjectAsync method","IWbemServices.GetObjectAsync","IWbemServices::GetObjectAsync","WBEM_FLAG_DIRECT_READ","WBEM_FLAG_SEND_STATUS","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_getobjectasync","wbemcli/IWbemServices::GetObjectAsync","wmi.iwbemservices_getobjectasync"]
old-location: wmi\iwbemservices_getobjectasync.htm
tech.root: wmi
ms.assetid: 6868a14d-3776-43a0-b241-b40d42a97afc
ms.date: 12/05/2018
ms.keywords: GetObjectAsync, GetObjectAsync method [Windows Management Instrumentation], GetObjectAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],GetObjectAsync method, IWbemServices.GetObjectAsync, IWbemServices::GetObjectAsync, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_SEND_STATUS, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_getobjectasync, wbemcli/IWbemServices::GetObjectAsync, wmi.iwbemservices_getobjectasync
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
 - IWbemServices::GetObjectAsync
 - wbemcli/IWbemServices::GetObjectAsync
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
 - IWbemServices.GetObjectAsync
---

# IWbemServices::GetObjectAsync


## -description

The 
<b>IWbemServices::GetObjectAsync</b> method retrieves an object, either a class definition or instance, based on its path. This is similar to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> except that the call returns immediately, and the object is provided to the supplied object sink.

Currently, this method retrieves objects only from the namespace associated with the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> pointer.

## -parameters

### -param strObjectPath [in]

Path of the object to retrieve. For an instance provider, <i>StrObjectPath</i> can be in the following format:

<ul>
<li>Namespace:Class.Key = "Value"</li>
<li>Namespace:Class = "Value"</li>
<li>Namespace:Class.Key = "Value", Key2 = "Value2"</li>
</ul>
Specifying the namespace before the class is optional. Object paths without namespaces refer to instances in the current namespace. If necessary, you can substitute the single-quotation mark character (') for the double-quotation mark character (") to delimit the start and end of string property types.

If this is <b>NULL</b>, an empty object, which can become a new class, is returned. For more information, see 
<a href="/windows/desktop/WmiSdk/creating-a-class">Creating a Class</a>.

### -param lFlags [in]

The following flags affect the behavior of this method.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without any regard to its parent class or subclasses.



#### WBEM_FLAG_SEND_STATUS

Registers a request to receive intermediate status reports through the client's implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting for this flag to change behavior.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that can be used by the provider that produces the requested class or instance. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pResponseHandler [in]

Pointer to the caller's implementation of 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a>. This handler receives the requested object when it becomes available through the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> method. The <i>pObjParam</i> parameter contains the object. If any error code is returned, then the supplied 
<b>IWbemObjectSink</b> pointer is not used. If <b>WBEM_S_NO_ERROR</b> is returned, then the user's 
<b>IWbemObjectSink</b> implementation is called to indicate the result of the operation. Windows Management only calls AddRef to the pointer in cases where <b>WBEM_S_NO_ERROR</b> returns. In cases where an error code returns, the reference count is the same as on entry. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a><b>GetErrorInfo</b>.

COM-specific error codes can also be returned if network problems cause you to lose the remote connection to Windows Management.

## -remarks

When implementing an instance provider, you should use the object path parser sample code in the WMI section of the PSDK to parse the object path for recognizing which object the client requests. Further, a provider that supports a derived class need only supply the values for the local properties of the class, rather than the inherited properties. WMI requests that the provider of the base class handle inherited properties.

When implementing a class provider, 
<b>GetObjectAsync</b> must determine which class is being requested by parsing the class name object path stored in the <i>strObjectPath</i> parameter. The 
<b>GetObjectAsync</b> method then either builds the class dynamically or takes the class from a private cache. Then, 
<b>GetObjectAsync</b> sends the class to WMI using the 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> pointer pointed to by the <i>pResponseHandler</i> parameter. The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. It can also be called with no intervening calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> if error conditions occur.

Because the call-back might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

For more information about using methods semisynchronously, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> and <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.


#### Examples

The following example describes how to implement 
<b>GetObjectAsync</b> for an instance provider.


```cpp
SCODE CInstPro::GetObjectAsync (BSTR ObjectPath, 
                                long lFlags, IWbemContext *pCtx,
                                IWbemObjectSink FAR* pHandler)
{
    ULONG cRef;         // Reference count
    SCODE sc;
    BOOL bOK = FALSE;

    IWbemServices *  m_pNamespace;
    IWbemClassObject FAR* pObj;

    // Check arguments.

    if(ObjectPath == NULL || pHandler == NULL ||
        m_pNamespace == NULL)
        return WBEM_E_INVALID_PARAMETER;

    
    // Based on the object path, produce an empty instance
    // of the class and gather required data,
    // setting the instance's property values accordingly.
    // This example assumes that GetByPath is implemented
    // by the provider to do this.
    // The IWbemPath interface can be used to parse
    // the object path, separating the namespace and class name.

    sc = GetByPath (ObjectPath, &pObj, pCtx);
    if(sc == S_OK) 
    {
        pHandler->Indicate (1, &pObj);
        pObj->Release();
        bOK = TRUE;
    }

    sc = (bOK) ? S_OK : WBEM_E_NOT_FOUND;

    // Set status.

    pHandler->SetStatus(0,sc, NULL, NULL);

    // Free memory resources.

    SysFreeString(ObjectPath);
    m_pNamespace->Release();
    pObj->Release();

    return sc;
  
}
```


The following example shows how a typical class provider  implements 
<b>GetObjectAsync</b>.


```cpp
HRESULT CStdProvider::GetObjectAsync( 
            /* [in] */ BSTR strObjectPath,
            /* [in] */ long lFlags,
            /* [in] */ IWbemContext __RPC_FAR *pCtx,
            /* [in] */ IWbemObjectSink __RPC_FAR *pResponseHandler
            )
{

    IWbemClassObject *pClass = 0;

// Assume there is an IWbemServices pointer available.
// Retrieve an 'empty' object which is built up
// into the class definition.

    HRESULT hRes = m_pSvc->GetObject(NULL, 0, NULL, &pClass, 0);
    if (hRes)
        return hRes;

// Parse the object path and determine which class is   
// required. The path string is the required class name.
// Fill in the properties required for the class definition
// using pClass->Put(...), and so on.

    
    // ...

    // Send the class definition back to WMI.
    pResponseHandler->Indicate(1, &pClass);

// Indicate that it is now finished.

    pResponseHandler->SetStatus(0, WBEM_S_NO_ERROR, 0, 0);
    SysFreeString(strObjectPath);
    m_pSvc->Release();
    pClass->Release();  // This is no longer needed.
    return WBEM_S_NO_ERROR;
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/WmiSdk/creating-a-class">Creating a Class</a>



<a href="/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object">Describing the Location of a WMI Object</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a>