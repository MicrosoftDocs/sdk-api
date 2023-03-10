---
UID: NF:wbemcli.IWbemServices.GetObject
title: IWbemServices::GetObject (wbemcli.h)
description: The IWbemServices::GetObject method retrieves a class or instance. This method only retrieves objects from the namespace associated with the current IWbemServices object.
helpviewer_keywords: ["GetObject","GetObject method [Windows Management Instrumentation]","GetObject method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","GetObject method","IWbemServices.GetObject","IWbemServices::GetObject","WBEM_FLAG_DIRECT_READ","WBEM_FLAG_RETURN_IMMEDIATELY","WBEM_FLAG_RETURN_WBEM_COMPLETE","WBEM_FLAG_USE_AMENDED_QUALIFIERS","_hmm_iwbemservices_getobject","wbemcli/IWbemServices::GetObject","wmi.iwbemservices_getobject"]
old-location: wmi\iwbemservices_getobject.htm
tech.root: wmi
ms.assetid: 68150273-c4ec-46f1-a3e6-d7169824b69d
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Windows Management Instrumentation], GetObject method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],GetObject method, IWbemServices.GetObject, IWbemServices::GetObject, WBEM_FLAG_DIRECT_READ, WBEM_FLAG_RETURN_IMMEDIATELY, WBEM_FLAG_RETURN_WBEM_COMPLETE, WBEM_FLAG_USE_AMENDED_QUALIFIERS, _hmm_iwbemservices_getobject, wbemcli/IWbemServices::GetObject, wmi.iwbemservices_getobject
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
 - IWbemServices::GetObject
 - wbemcli/IWbemServices::GetObject
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
 - IWbemServices.GetObject
---

# IWbemServices::GetObject


## -description

The 
<b>IWbemServices::GetObject</b> method retrieves a class or instance. This method only retrieves objects from the namespace associated with the current 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> object.

## -parameters

### -param strObjectPath [in]

Path of the object to retrieve. If this is <b>NULL</b>, an empty object is returned that can become a new class. For more information, see 
<a href="/windows/desktop/WmiSdk/creating-a-class">Creating a Class</a>.

### -param lFlags [in]

The following flags affect the behavior of this method.



#### WBEM_FLAG_USE_AMENDED_QUALIFIERS

If this flag is set, WMI retrieves the amended qualifiers stored in the localized namespace of the current connection's locale. If not set, only the qualifiers stored in the immediate namespace are retrieved.



#### WBEM_FLAG_RETURN_WBEM_COMPLETE

This flag makes this a synchronous call.



#### WBEM_FLAG_RETURN_IMMEDIATELY

This flag makes this a semisynchronous call. You must provide a valid pointer for the <i>ppCallResult</i> parameter. For more information, see 
<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.



#### WBEM_FLAG_DIRECT_READ

This flag causes direct access to the provider for the class specified without any regard to its parent class or subclasses.

### -param pCtx [in]

Typically <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider that is producing the requested class or instance. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppObject [out]

If not <b>NULL</b>, this receives the object, if it is found. The returned object has a positive reference count. The caller must use <b>Release</b> when the object is no longer needed. In all cases of error, this parameter is set to point to <b>NULL</b>.

### -param ppCallResult [out]

If <b>NULL</b>, this parameter is not used. If the <i>lFlags</i> parameter contains <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, this call returns immediately with <b>WBEM_S_NO_ERROR</b>. The <i>ppCallResult</i> parameter receives a pointer to a new 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a> object, which can then be polled to obtain the result using the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus">GetCallStatus</a> method. The caller can call 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getresultobject">IWbemCallResult::GetResultObject</a> to retrieve the object when it becomes available.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/desktop/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.

## -see-also

<a href="/windows/desktop/WmiSdk/creating-a-class">Creating a Class</a>



<a href="/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object">Describing the Location of a WMI Object</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult">IWbemCallResult</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync">IWbemServices::GetObjectAsync</a>



<a href="/windows/desktop/WmiSdk/retrieving-an-error-code">Retrieving an Error Code</a>