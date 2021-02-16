---
UID: NF:wbemcli.IWbemClassObject.BeginMethodEnumeration
title: IWbemClassObject::BeginMethodEnumeration (wbemcli.h)
description: Use the IWbemClassObject::BeginMethodEnumeration method call to begin an enumeration of the methods available for the object.
helpviewer_keywords: ["BeginMethodEnumeration","BeginMethodEnumeration method [Windows Management Instrumentation]","BeginMethodEnumeration method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","BeginMethodEnumeration method","IWbemClassObject.BeginMethodEnumeration","IWbemClassObject::BeginMethodEnumeration","WBEM_FLAG_LOCAL_ONLY","WBEM_FLAG_PROPAGATED_ONLY","_hmm_iwbemclassobject_beginmethodenumeration","wbemcli/IWbemClassObject::BeginMethodEnumeration","wmi.iwbemclassobject_beginmethodenumeration"]
old-location: wmi\iwbemclassobject_beginmethodenumeration.htm
tech.root: wmi
ms.assetid: 3d8656d7-37e5-4921-906e-c82f8878cd90
ms.date: 12/05/2018
ms.keywords: BeginMethodEnumeration, BeginMethodEnumeration method [Windows Management Instrumentation], BeginMethodEnumeration method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],BeginMethodEnumeration method, IWbemClassObject.BeginMethodEnumeration, IWbemClassObject::BeginMethodEnumeration, WBEM_FLAG_LOCAL_ONLY, WBEM_FLAG_PROPAGATED_ONLY, _hmm_iwbemclassobject_beginmethodenumeration, wbemcli/IWbemClassObject::BeginMethodEnumeration, wmi.iwbemclassobject_beginmethodenumeration
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
 - IWbemClassObject::BeginMethodEnumeration
 - wbemcli/IWbemClassObject::BeginMethodEnumeration
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
 - IWbemClassObject.BeginMethodEnumeration
---

# IWbemClassObject::BeginMethodEnumeration


## -description

Use the 
<b>IWbemClassObject::BeginMethodEnumeration</b> method call to begin an enumeration of the methods available for the object.

This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointers which point to CIM instances. The order in which methods are enumerated is guaranteed to be invariant for a given instance of 
<b>IWbemClassObject</b>.

## -parameters

### -param lEnumFlags [in]

Specifies the scope of the enumeration.


Possible values:





#### WBEM_FLAG_LOCAL_ONLY

Only include methods that are defined in the class itself.



#### WBEM_FLAG_PROPAGATED_ONLY

Only include methods that are inherited from parent classes.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-nextmethod">IWbemClassObject::NextMethod</a>