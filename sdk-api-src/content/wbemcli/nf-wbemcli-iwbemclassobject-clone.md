---
UID: NF:wbemcli.IWbemClassObject.Clone
title: IWbemClassObject::Clone (wbemcli.h)
description: The IWbemClassObject::Clone method returns a new object that is a complete clone of the current object. The new object has a COM reference count of 1.
helpviewer_keywords: ["Clone","Clone method [Windows Management Instrumentation]","Clone method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","Clone method","IWbemClassObject.Clone","IWbemClassObject::Clone","_hmm_iwbemclassobject_clone","wbemcli/IWbemClassObject::Clone","wmi.iwbemclassobject_clone"]
old-location: wmi\iwbemclassobject_clone.htm
tech.root: wmi
ms.assetid: 4a708963-f677-4419-800d-02a01908e7cb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Management Instrumentation], Clone method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],Clone method, IWbemClassObject.Clone, IWbemClassObject::Clone, _hmm_iwbemclassobject_clone, wbemcli/IWbemClassObject::Clone, wmi.iwbemclassobject_clone
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
 - IWbemClassObject::Clone
 - wbemcli/IWbemClassObject::Clone
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
 - IWbemClassObject.Clone
---

# IWbemClassObject::Clone


## -description

The 
<b>IWbemClassObject::Clone</b> method returns a new object that is a complete clone of the current object. The new object has a COM reference count of 1.

## -parameters

### -param ppCopy [out]

This parameter cannot be <b>NULL</b>. It receives the copy of the current object. You must call <b>IWbemClassObject::Release</b> on this object when it is no longer required.

A new object is not returned on error.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

Use this method to duplicate a class definition, or to duplicate an instance. This can be useful when the original copy of the object is required for backup purposes while a new copy is modified. Likewise, use this method to create many new instances from a single source instance. For example, use 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-spawninstance">IWbemClassObject::SpawnInstance</a> to create a single starting instance, and use 
<b>IWbemClassObject::Clone</b> to produce 100 copies of the instance quickly. Each object can be modified subsequently to take on its particular values.

It is not possible to use this method to convert a class definition into an instance, or convert an instance into a class definition.