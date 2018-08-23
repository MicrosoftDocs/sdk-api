---
UID: NF:wbemcli.IWbemServices.ExecMethod
title: IWbemServices::ExecMethod
author: windows-sdk-content
description: Executes a method exported by a CIM object.
old-location: wmi\iwbemservices_execmethod.htm
old-project: WmiSdk
ms.assetid: 9acba1aa-bcca-416a-863c-704d2e72df07
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ExecMethod, ExecMethod method [Windows Management Instrumentation], ExecMethod method [Windows Management Instrumentation],IWbemServices interface, IWbemServices interface [Windows Management Instrumentation],ExecMethod method, IWbemServices.ExecMethod, IWbemServices::ExecMethod, _hmm_iwbemservices_execmethod, wbemcli/IWbemServices::ExecMethod, wmi.iwbemservices_execmethod
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
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
 - IWbemServices.ExecMethod
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Esscli.dll; FrameDyn.dll; FrameDynOS.dll; Ntevt.dll; Stdprov.dll; Viewprov.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wbemsvc.dll; Wmipicmp.dll; Wmidcprv.dll; Wmipjobj.dll; Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemServices::ExecMethod


## -description


The 
<b>IWbemServices::ExecMethod</b> method executes a method exported by a CIM object. The method call is forwarded to the appropriate provider where it executes. Information and status are returned to the caller, which blocks until the call is complete.

Methods are not directly implemented by Windows Management, but are exported by method providers. For any given CIM class, the available methods and their parameters must be specified in the documentation for the provider in question.

For more information about executing methods, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


## -parameters




### -param strObjectPath [in]

Valid <b>BSTR</b> containing the 
<a href="https://msdn.microsoft.com/5ae95707-d023-4102-9b41-140c54b0c5b7">object path</a> of the object for which the method is executed.


### -param strMethodName [in]

Name of the method for the object.


### -param lFlags [in]

This parameter can be set to 0 to make this a synchronous call. To make this a semisynchronous call, set <i>lFlags</i> to <b>WBEM_FLAG_RETURN_IMMEDIATELY</b>, provide a valid pointer for the <i>ppCallResult</i> parameter, and this call returns immediately. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


### -param pCtx [in]

Typically <b>NULL</b>;  otherwise, this is a pointer to an 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object that may be used by the provider executing the method. The values in the context object must be specified in the documentation for the provider in question. For more information about this parameter, see 
<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>.


### -param pInParams [in]

May be <b>NULL</b> if no in-parameters are required to execute the method. Otherwise, this points to an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> that contains the properties acting as inbound parameters for the method execution. The contents of the object are method-specific, and are part of the specification for the provider in question. For more information about constructing input parameters, see <a href="https://msdn.microsoft.com/17b72ceb-e730-4176-aa4d-189d0b6acc8b">Creating Parameters Objects in C++</a>.


### -param ppOutParams [out]

If not <b>NULL</b>, receives a pointer to the outbound parameters and return values for the method execution. The contents of this object are method-specific, and are part of the specification for the provider in question. The caller must call <a href="_com_iunknown_release">Release</a> on the returned object when it is no longer required.


### -param ppCallResult [out]

If <b>NULL</b>, this is not used. If <i>ppCallResult</i> is specified, it must be set to point to <b>NULL</b> on entry. In this case, the call returns immediately with <b>WBEM_S_NO_ERROR</b>. The <i>ppCallResult</i> parameter receives a pointer to a new 
<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a> object, which must be polled to obtain the result of the method execution using the 
<a href="https://msdn.microsoft.com/5a600fd8-87d8-446d-93da-5b22fd575a11">GetCallStatus</a> method. The out parameters for the call are available by calling 
<a href="https://msdn.microsoft.com/06603f26-587f-4aff-8ae3-7f77f9b266f5">IWbemCallResult::GetResultObject</a>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

On failure, you can obtain any available information from the COM function <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

COM-specific error codes also may be returned if network problems cause you to lose the remote connection to Windows Management.




## -remarks



If <i>ppOutParams</i> is not <b>NULL</b>, the client can determine the method's return value type by examining the <b>ReturnValue</b> property of the object pointed to by <i>ppOutParams</i>.




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/06603f26-587f-4aff-8ae3-7f77f9b266f5">IWbemCallResult::GetResultObject</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/61966c03-80dc-4556-b2fc-97e879cf458c">IWbemServices::ExecMethodAsync</a>
 

 

