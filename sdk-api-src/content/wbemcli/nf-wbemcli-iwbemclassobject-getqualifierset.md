---
UID: NF:wbemcli.IWbemClassObject.GetQualifierSet
title: IWbemClassObject::GetQualifierSet (wbemcli.h)
description: The IWbemClassObject::GetQualifierSet method returns an interface pointer that allows read and write operations on the set of qualifiers for the entire class object, whether the object is an instance or a class definition.
helpviewer_keywords: ["GetQualifierSet","GetQualifierSet method [Windows Management Instrumentation]","GetQualifierSet method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","GetQualifierSet method","IWbemClassObject.GetQualifierSet","IWbemClassObject::GetQualifierSet","_hmm_iwbemclassobject_getqualifierset","wbemcli/IWbemClassObject::GetQualifierSet","wmi.iwbemclassobject_getqualifierset"]
old-location: wmi\iwbemclassobject_getqualifierset.htm
tech.root: wmi
ms.assetid: da86b723-8126-44b9-95ec-120d88390ef3
ms.date: 12/05/2018
ms.keywords: GetQualifierSet, GetQualifierSet method [Windows Management Instrumentation], GetQualifierSet method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetQualifierSet method, IWbemClassObject.GetQualifierSet, IWbemClassObject::GetQualifierSet, _hmm_iwbemclassobject_getqualifierset, wbemcli/IWbemClassObject::GetQualifierSet, wmi.iwbemclassobject_getqualifierset
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
 - IWbemClassObject::GetQualifierSet
 - wbemcli/IWbemClassObject::GetQualifierSet
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
 - IWbemClassObject.GetQualifierSet
---

# IWbemClassObject::GetQualifierSet


## -description

The 
<b>IWbemClassObject::GetQualifierSet</b> method returns an interface pointer that allows read and write operations on the set of qualifiers for the entire class object, whether the object is an instance or a class definition. Any qualifiers added, deleted, or edited using the returned pointer apply to the entire instance or class definition.

## -parameters

### -param ppQualSet [out]

Receives the interface pointer that allows access to the qualifiers for the class object. The returned object has a positive reference count upon return from the call. The caller must call <b>IWbemQualifierSet::Release</b> when the object is no longer needed. This parameter cannot be <b>NULL</b>. On error, a new object is not returned and the pointer is left unmodified.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset">IWbemClassObject::GetPropertyQualifierSet</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a>