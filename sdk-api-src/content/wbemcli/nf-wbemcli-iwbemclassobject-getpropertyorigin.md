---
UID: NF:wbemcli.IWbemClassObject.GetPropertyOrigin
title: IWbemClassObject::GetPropertyOrigin (wbemcli.h)
description: The IWbemClassObject::GetPropertyOrigin method retrieves the name of the class in which a particular property was introduced.
helpviewer_keywords: ["GetPropertyOrigin","GetPropertyOrigin method [Windows Management Instrumentation]","GetPropertyOrigin method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","GetPropertyOrigin method","IWbemClassObject.GetPropertyOrigin","IWbemClassObject::GetPropertyOrigin","_hmm_iwbemclassobject_getpropertyorigin","wbemcli/IWbemClassObject::GetPropertyOrigin","wmi.iwbemclassobject_getpropertyorigin"]
old-location: wmi\iwbemclassobject_getpropertyorigin.htm
tech.root: wmi
ms.assetid: 05228d88-baa2-4e89-a8c8-139f9ffea86c
ms.date: 12/05/2018
ms.keywords: GetPropertyOrigin, GetPropertyOrigin method [Windows Management Instrumentation], GetPropertyOrigin method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetPropertyOrigin method, IWbemClassObject.GetPropertyOrigin, IWbemClassObject::GetPropertyOrigin, _hmm_iwbemclassobject_getpropertyorigin, wbemcli/IWbemClassObject::GetPropertyOrigin, wmi.iwbemclassobject_getpropertyorigin
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
 - IWbemClassObject::GetPropertyOrigin
 - wbemcli/IWbemClassObject::GetPropertyOrigin
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
 - IWbemClassObject.GetPropertyOrigin
---

# IWbemClassObject::GetPropertyOrigin


## -description

The 
<b>IWbemClassObject::GetPropertyOrigin</b> method retrieves the name of the class in which a particular property was introduced. For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes. If the object does not inherit from a parent class, as in the case of a base class, for example, then the current class name is returned.

## -parameters

### -param wszName [in]

Property name for which the owning class name is desired. This must point to a valid <b>LPCWSTR</b>, which is treated as read-only.

### -param pstrClassName [out]

Pointer to the address of a new <b>BSTR</b> that receives the parent class name. To prevent memory leaks in the client process, the caller must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when the name is no longer required. This parameter must not point to a valid string before the method is called because this is an output parameter, and this pointer is not deallocated after the call is complete.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-inheritsfrom">IWbemClassObject::InheritsFrom</a>