---
UID: NF:wbemcli.IWbemServices.ExecMethodAsync
title: IWbemServices::ExecMethodAsync (wbemcli.h)
description: Asynchronously executes a method exported by a CIM object.
helpviewer_keywords: ["ExecMethodAsync","ExecMethodAsync method [Windows Management Instrumentation]","ExecMethodAsync method [Windows Management Instrumentation]","IWbemServices interface","IWbemServices interface [Windows Management Instrumentation]","ExecMethodAsync method","IWbemServices.ExecMethodAsync","IWbemServices::ExecMethodAsync","_hmm_iwbemservices_execmethodasync","wbemcli/IWbemServices::ExecMethodAsync","wmi.iwbemservices_execmethodasync"]
old-location: wmi\iwbemservices_execmethodasync.htm
tech.root: wmi
ms.assetid: 61966c03-80dc-4556-b2fc-97e879cf458c
ms.date: 12/05/2018
ms.keywords: ExecMethodAsync, ExecMethodAsync method [Windows Management Instrumentation], ExecMethodAsync method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecMethodAsync method, IWbemServices.ExecMethodAsync, IWbemServices::ExecMethodAsync, _hmm_iwbemservices_execmethodasync, wbemcli/IWbemServices::ExecMethodAsync, wmi.iwbemservices_execmethodasync
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
 - IWbemServices::ExecMethodAsync
 - wbemcli/IWbemServices::ExecMethodAsync
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
 - IWbemServices.ExecMethodAsync
---

# IWbemServices::ExecMethodAsync


## -description

The 
<b>IWbemServices::ExecMethodAsync</b> method asynchronously executes a method exported by a CIM object. The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where it executes. Information and status are returned to the caller through the supplied object sink.

Methods are not directly implemented by Windows Management, but are exported by method providers. For any given CIM class, the available methods and their parameters are part of the documentation for the provider in question.

## -parameters

### -param strObjectPath [in]

Valid <b>BSTR</b> containing the 
<a href="/windows/desktop/WmiSdk/describing-a-class-object-path">object path</a> of the object for which the method is to be executed. You can invoke a static method using either a class name or an object path to an instance. The method provider can parse the object path parameter to determine the class and instance that contain the method definition.

### -param strMethodName [in]

Name of the method for the object.

### -param lFlags [in]

<b>WBEM_FLAG_SEND_STATUS</b> registers with Windows Management a request to receive intermediate status reports through the clients implementation of 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a>. Provider implementation must support intermediate status reporting for this flag to change behavior. Note that the <b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b> flag cannot be used here.

### -param pCtx [in]

Typically <b>NULL</b>;  otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object that may be used by the provider executing the method. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param pInParams [in]

Can be <b>NULL</b> if no inbound parameters are required to execute the method. Otherwise, this points to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object that contains the properties acting as inbound parameters for the method execution. The contents of the object are method-specific, and are part of the specification for the provider in question. However, the most common object is an instance of the <a href="/windows/desktop/WmiSdk/--parameters">__Parameters</a> system class. For each input parameter to the method to be called, there is one non-system property. Method providers ignore the <a href="/windows/desktop/WmiSdk/standard-wmi-qualifiers">ID</a> qualifiers attached to each parameter in the method, which are typically used only by browsers and similar applications.

### -param pResponseHandler [in]

Cannot be <b>NULL</b>. The object sink receives the result of the method call. The outbound parameters are sent to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a>. The most common returned object is an instance of the <a href="/windows/desktop/WmiSdk/--parameters">__Parameters</a> system class. For more information about return codes, see the Remarks section. When implementing a method provider, you should call 
<b>Indicate</b> to return output parameter information before calling 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> to report the final status.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="/windows/win32/api/oleauto/nf-oleauto-geterrorinfo">GetErrorInfo</a>.

Other errors are reported asynchronously to the object sink supplied in the <i>pReponseHandler</i> parameter.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to WMI.

## -remarks

A single method provider can supply methods for many classes and instances. Method providers have to deal with a maximum of three return values.

The 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-setstatus">IWbemObjectSink::SetStatus</a> method is called to indicate the end of the result set. It may also be called with no intervening calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">IWbemObjectSink::Indicate</a> if error conditions occur.

Because the call-back might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication. If you require asynchronous communication, see <a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>.

<table>
<tr>
<th>Return values</th>
<th>Description</th>
</tr>
<tr>
<td>
<b>ExecMethodAsync</b> (required)

</td>
<td>
Indicates whether or not the input parameters for the method that are pointed to by the <b>pInParams</b> parameter are valid.

</td>
</tr>
<tr>
<td>
Invoked method (optional)

</td>
<td>
Dependent on the method. The return value is placed in the <b>ReturnValue</b> property of the 
<a href="/windows/desktop/WmiSdk/--parameters">__PARAMETERS</a> instance representing the out parameters and returned through a call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a>.

</td>
</tr>
<tr>
<td>
Invoked method out parameters (optional)

</td>
<td>
Dependent on the method. Out parameters are placed in non-system properties of a 
<a href="/windows/desktop/WmiSdk/--parameters">__PARAMETERS</a> instance and returned through 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectsink-indicate">Indicate</a>.

</td>
</tr>
</table>
 


#### Examples

The following C++ example shows how to implement the 
     <b>IWbemServices::ExecMethodAsync</b> method for the <b>Echo</b> method of the <b>TestMeth</b> class. The <b>TestMeth</b> class supports a method that has one input parameter and one output parameter and that returns an unsigned 32-bit integer. The implementation assumes that there is only one method called <b>Echo</b> and one class that contains it.  For the sake of brevity, there is no error checking or object path parsing.


```cpp
STDMETHODIMP CMyMethodProvider::ExecMethodAsync(BSTR ObjectPath, 
    BSTR MethodName, long lFlags, IWbemContext* pCtx, 
    IWbemClassObject* pInParams, IWbemObjectSink* pResultSink)
{
    HRESULT hr;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutClass = NULL;
    IWbemClassObject* pOutParams;

    // Allocate some BSTRs.

    BSTR ClassName = SysAllocString(L"TestMeth");    
    BSTR InputArgName = SysAllocString(L"sInArg");
    BSTR OutputArgName = SysAllocString(L"sOutArg");
    BSTR retValName = SysAllocString(L"ReturnValue");

    // Get the class object; this is hard-coded and matches the class
    // in the MOF.  A more sophisticated example would parse 
    // ObjectPath to determine the class and possibly the instance.
    // The m_pWbemSvcs pointer is of type IWbemServices*
    hr = m_pWbemSvcs->GetObject(ClassName, 0, pCtx, &pClass, NULL);

    // This method returns values, and so creates an instance of the
    // output argument class.

    hr = pClass->GetMethod(MethodName, 0, NULL, &pOutClass);
    pOutClass->SpawnInstance(0, &pOutParams);

    // Copy the input argument into the output object.

    VARIANT var;
    VariantInit(&var);

    // Get the input argument.
    pInParams->Get(InputArgName, 0, &var, NULL, NULL);   

    // Put it into the output object.
    pOutParams->Put(OutputArgName , 0, &var, 0);      

    long lLen = wcslen(var.bstrVal);
    VariantClear(&var);
    var.vt = VT_I4;
    var.lVal = lLen;
    // Special name for the return value.
    pOutParams->Put(retValName , 0, &var, 0); 

    // Send the output object back to the client by the sink. Then 
    // release the pointers and free the strings.

    hr = pResultSink->Indicate(1, &pOutParams);
    pOutParams->Release();
    pOutClass->Release();
    pClass->Release();
    SysFreeString(ClassName);
    SysFreeString(InputArgName);
    SysFreeString(OutputArgName);
    SysFreeString(retValName);
 
    // All done; now set the status.

    hr = pResultSink->SetStatus(0,WBEM_S_NO_ERROR,NULL,NULL);
    return WBEM_S_NO_ERROR;
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/calling-a-method">Calling a Method</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcallresult-getresultobject">IWbemCallResult::GetResultObject</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync">IWbemServices::ExecMethodAsync</a>