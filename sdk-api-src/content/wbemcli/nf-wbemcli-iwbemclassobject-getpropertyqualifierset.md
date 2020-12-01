---
UID: NF:wbemcli.IWbemClassObject.GetPropertyQualifierSet
title: IWbemClassObject::GetPropertyQualifierSet (wbemcli.h)
description: The IWbemClassObject::GetPropertyQualifierSet method gets the qualifier set for a particular property in the class object. You can use this method with properties that are a member of an instance or a class definition.
helpviewer_keywords: ["GetPropertyQualifierSet","GetPropertyQualifierSet method [Windows Management Instrumentation]","GetPropertyQualifierSet method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","GetPropertyQualifierSet method","IWbemClassObject.GetPropertyQualifierSet","IWbemClassObject::GetPropertyQualifierSet","_hmm_iwbemclassobject_getpropertyqualifierset","wbemcli/IWbemClassObject::GetPropertyQualifierSet","wmi.iwbemclassobject_getpropertyqualifierset"]
old-location: wmi\iwbemclassobject_getpropertyqualifierset.htm
tech.root: wmi
ms.assetid: 4bfca42e-7688-42e1-afa3-24b7eaaad9fe
ms.date: 12/05/2018
ms.keywords: GetPropertyQualifierSet, GetPropertyQualifierSet method [Windows Management Instrumentation], GetPropertyQualifierSet method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetPropertyQualifierSet method, IWbemClassObject.GetPropertyQualifierSet, IWbemClassObject::GetPropertyQualifierSet, _hmm_iwbemclassobject_getpropertyqualifierset, wbemcli/IWbemClassObject::GetPropertyQualifierSet, wmi.iwbemclassobject_getpropertyqualifierset
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
 - IWbemClassObject::GetPropertyQualifierSet
 - wbemcli/IWbemClassObject::GetPropertyQualifierSet
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
 - IWbemClassObject.GetPropertyQualifierSet
---

# IWbemClassObject::GetPropertyQualifierSet


## -description

The 
<b>IWbemClassObject::GetPropertyQualifierSet</b> method gets the qualifier set for a particular property in the class object. You can use this method with properties that are a member of an instance or a class definition.

## -parameters

### -param wszProperty [in]

Property for which the qualifier set is requested. This cannot be <b>NULL</b> and must point to a valid <b>LPCWSTR</b>. The property can be local or propagated from the parent class. Note that system properties have no qualifiers so this method returns the error code <b>WBEM_E_SYSTEM_PROPERTY</b> if you attempt to obtain the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a> pointer for a system property.

### -param ppQualSet [out]

Receives an interface pointer that allows access to the qualifiers for the named property. The caller must call <b>IWbemQualifierSet::Release</b> on the pointer when access to the object is no longer required. The property is set to point to <b>NULL</b> when there are error conditions. A new object is not returned.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a>