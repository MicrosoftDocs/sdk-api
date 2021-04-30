---
UID: NF:wbemcli.IWbemClassObject.NextMethod
title: IWbemClassObject::NextMethod (wbemcli.h)
description: Used to retrieve the next method in a method enumeration sequence that starts with a call to IWbemClassObject::BeginMethodEnumeration.
helpviewer_keywords: ["IWbemClassObject interface [Windows Management Instrumentation]","NextMethod method","IWbemClassObject.NextMethod","IWbemClassObject::NextMethod","NextMethod","NextMethod method [Windows Management Instrumentation]","NextMethod method [Windows Management Instrumentation]","IWbemClassObject interface","_hmm_iwbemclassobject_nextmethod","wbemcli/IWbemClassObject::NextMethod","wmi.iwbemclassobject_nextmethod"]
old-location: wmi\iwbemclassobject_nextmethod.htm
tech.root: wmi
ms.assetid: 4c11e043-518b-46f6-bb39-e80354ef2c8a
ms.date: 12/05/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],NextMethod method, IWbemClassObject.NextMethod, IWbemClassObject::NextMethod, NextMethod, NextMethod method [Windows Management Instrumentation], NextMethod method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_nextmethod, wbemcli/IWbemClassObject::NextMethod, wmi.iwbemclassobject_nextmethod
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
 - IWbemClassObject::NextMethod
 - wbemcli/IWbemClassObject::NextMethod
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
 - IWbemClassObject.NextMethod
---

# IWbemClassObject::NextMethod


## -description

The 
<b>IWbemClassObject::NextMethod</b> method is used to retrieve the next method in a method enumeration sequence that starts with 
a call to  <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginmethodenumeration">IWbemClassObject::BeginMethodEnumeration</a>.

This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointers that point to CIM instances.

## -parameters

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param pstrName [out]

A pointer that should point to <b>NULL</b> prior to the call. This parameter receives the address of a <b>BSTR</b> value containing the method name. The caller must release the string using <b>SysFreeString</b> when it is no longer required.

### -param ppInSignature [out]

A pointer that receives a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> containing the in parameters for the method.

### -param ppOutSignature [out]

A pointer that receives a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> containing the out parameters for the method.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The caller begins the enumeration sequence using 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginmethodenumeration">IWbemClassObject::BeginMethodEnumeration</a>, and then calls 
<b>IWbemClassObject::NextMethod</b> until <b>WBEM_S_NO_MORE_DATA</b> is returned. The caller, optionally, finishes the sequence with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endmethodenumeration">IWbemClassObject::EndMethodEnumeration</a>. The caller may terminate the enumeration early by calling 
<b>IWbemClassObject::EndMethodEnumeration</b> at any time.

<div class="alert"><b>Note</b>  The caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IWbemClassObject::Release</a> on the <i>ppInSignature</i> and <i>ppOutSignature</i> pointers when these objects are no longer required.</div>
<div> </div>