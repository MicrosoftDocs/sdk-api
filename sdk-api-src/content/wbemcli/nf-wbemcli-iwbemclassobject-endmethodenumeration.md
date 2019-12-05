---
UID: NF:wbemcli.IWbemClassObject.EndMethodEnumeration
title: IWbemClassObject::EndMethodEnumeration (wbemcli.h)
description: The IWbemClassObject::EndMethodEnumeration method is used to terminate a method enumeration sequence started with IWbemClassObject::BeginMethodEnumeration.
old-location: wmi\iwbemclassobject_endmethodenumeration.htm
tech.root: WmiSdk
ms.assetid: 7a6de467-65f7-4873-a2dd-9c52c138b1d2
ms.date: 12/05/2018
ms.keywords: EndMethodEnumeration, EndMethodEnumeration method [Windows Management Instrumentation], EndMethodEnumeration method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],EndMethodEnumeration method, IWbemClassObject.EndMethodEnumeration, IWbemClassObject::EndMethodEnumeration, _hmm_iwbemclassobject_endmethodenumeration, wbemcli/IWbemClassObject::EndMethodEnumeration, wmi.iwbemclassobject_endmethodenumeration
ms.topic: method
f1_keywords:
- wbemcli/IWbemClassObject.EndMethodEnumeration
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
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
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
- IWbemClassObject.EndMethodEnumeration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemClassObject::EndMethodEnumeration


## -description


The 
<b>IWbemClassObject::EndMethodEnumeration</b> method is used to terminate a method enumeration sequence started with 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginmethodenumeration">IWbemClassObject::BeginMethodEnumeration</a>.

This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointers which point to CIM instances.


## -parameters






## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



The caller begins the enumeration sequence using 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginmethodenumeration">IWbemClassObject::BeginMethodEnumeration</a>, and then calls 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-nextmethod">IWbemClassObject::NextMethod</a> until <b>WBEM_S_NO_MORE_DATA</b> is returned. The caller optionally finishes the sequence with 
<b>IWbemClassObject::EndMethodEnumeration</b>. The caller may terminate the enumeration early by calling 
<b>IWbemClassObject::EndMethodEnumeration</b> at any time.



