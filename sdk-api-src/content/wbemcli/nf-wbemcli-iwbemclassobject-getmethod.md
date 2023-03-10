---
UID: NF:wbemcli.IWbemClassObject.GetMethod
title: IWbemClassObject::GetMethod (wbemcli.h)
description: Returns information about the requested method.
helpviewer_keywords: ["GetMethod","GetMethod method [Windows Management Instrumentation]","GetMethod method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","GetMethod method","IWbemClassObject.GetMethod","IWbemClassObject::GetMethod","_hmm_iwbemclassobject_getmethod","wbemcli/IWbemClassObject::GetMethod","wmi.iwbemclassobject_getmethod"]
old-location: wmi\iwbemclassobject_getmethod.htm
tech.root: wmi
ms.assetid: d4775fe0-62bf-40a6-8e2c-7bc8c3d92e1f
ms.date: 12/05/2018
ms.keywords: GetMethod, GetMethod method [Windows Management Instrumentation], GetMethod method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetMethod method, IWbemClassObject.GetMethod, IWbemClassObject::GetMethod, _hmm_iwbemclassobject_getmethod, wbemcli/IWbemClassObject::GetMethod, wmi.iwbemclassobject_getmethod
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemClassObject::GetMethod
 - wbemcli/IWbemClassObject::GetMethod
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CIMWin32.dll
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipiprt.dll
api_name:
 - IWbemClassObject.GetMethod
---

# IWbemClassObject::GetMethod


## -description

The 
<b>IWbemClassObject::GetMethod</b> method returns information about the requested method. This call is only supported if the current object is a CIM class definition. Method information is not available from 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointers which point to CIM instances.

## -parameters

### -param wszName [in]

The method name. This cannot be <b>NULL</b>, and must point to a valid <b>LPCWSTR</b>.

### -param lFlags [in]

Reserved. This parameter must be 0.

### -param ppInSignature [out]

A pointer that receives an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointer which describes the in parameters to the method. This parameter is  ignored if set to <b>NULL</b>. Be aware that Windows Management can set the 
<b>IWbemClassObject</b> pointer to <b>NULL</b> if this method has no in parameters. For more information, see Remarks.

### -param ppOutSignature [out]

A pointer that receives an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointer which describes the out-parameters to the method. This parameter will be ignored if set to <b>NULL</b>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

For a method, the in and out parameters are described as properties in an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>, an instance of the system class 
<a href="/windows/desktop/WmiSdk/--parameters">__Parameters</a>.

For example, consider the following method:


```
Class MyClass{
    [key] string KeyVal;
    sint32 PropVal;
    sint32 ExampleMethod([in] sint32 Parm1, [in] uint32 Parm2, 
      [out] string Parm3);
};
```


In this example, the class has a single method. When the user calls 
<b>IWbemClassObject::GetMethod</b>, the <i>ppInSignature</i> parameter receives an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object, which contains two properties: <b>Parm1</b> and <b>Parm2</b>. The <i>ppOutSignature</i> parameter contains two properties, <b>Parm3</b> and <b>ReturnValue</b>.

After filling in the property values of the <i>ppInSignature</i> object, the caller can use the object to execute the method by calling 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a> or 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync">IWbemServices::ExecMethodAsync</a>.

<div class="alert"><b>Note</b>  The caller must call <b>IWbemClassObject::Release</b> on the <i>ppInSignature</i> and <i>ppOutSignature</i> pointers when these objects are no longer required.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-putmethod">IWbemClassObject::PutMethod</a>