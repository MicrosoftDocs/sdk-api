---
UID: NF:wbemcli.IWbemClassObject.GetMethodOrigin
title: IWbemClassObject::GetMethodOrigin (wbemcli.h)
description: The IWbemClassObject::GetMethodOrigin method is used to determine the class for which a method was declared.
helpviewer_keywords: ["GetMethodOrigin","GetMethodOrigin method [Windows Management Instrumentation]","GetMethodOrigin method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","GetMethodOrigin method","IWbemClassObject.GetMethodOrigin","IWbemClassObject::GetMethodOrigin","_hmm_iwbemclassobject_getmethodorigin","wbemcli/IWbemClassObject::GetMethodOrigin","wmi.iwbemclassobject_getmethodorigin"]
old-location: wmi\iwbemclassobject_getmethodorigin.htm
tech.root: wmi
ms.assetid: e3d55b1f-f9bd-40d1-9ad5-990c264524d5
ms.date: 12/05/2018
ms.keywords: GetMethodOrigin, GetMethodOrigin method [Windows Management Instrumentation], GetMethodOrigin method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetMethodOrigin method, IWbemClassObject.GetMethodOrigin, IWbemClassObject::GetMethodOrigin, _hmm_iwbemclassobject_getmethodorigin, wbemcli/IWbemClassObject::GetMethodOrigin, wmi.iwbemclassobject_getmethodorigin
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
 - IWbemClassObject::GetMethodOrigin
 - wbemcli/IWbemClassObject::GetMethodOrigin
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
 - IWbemClassObject.GetMethodOrigin
---

# IWbemClassObject::GetMethodOrigin


## -description

The 
<b>IWbemClassObject::GetMethodOrigin</b> method is used to determine the class for which a method was declared.

This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> pointers which point to CIM instances.

## -parameters

### -param wszMethodName [in]

Name of the method for the object whose owning class is being requested.

### -param pstrClassName [out]

Receives the name of the class which owns the method. The user must call <b>SysFreeString</b> on the returned <i>BSTR</i> when it is no longer required.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

Because methods are inherited from class to class, it is often desirable to determine the owning class for a given method.