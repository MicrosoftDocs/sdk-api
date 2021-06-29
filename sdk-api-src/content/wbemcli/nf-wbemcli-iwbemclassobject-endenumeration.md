---
UID: NF:wbemcli.IWbemClassObject.EndEnumeration
title: IWbemClassObject::EndEnumeration (wbemcli.h)
description: The IWbemClassObject::EndEnumeration method terminates an enumeration sequence started with IWbemClassObject::BeginEnumeration.
helpviewer_keywords: ["EndEnumeration","EndEnumeration method [Windows Management Instrumentation]","EndEnumeration method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","EndEnumeration method","IWbemClassObject.EndEnumeration","IWbemClassObject::EndEnumeration","_hmm_iwbemclassobject_endenumeration","wbemcli/IWbemClassObject::EndEnumeration","wmi.iwbemclassobject_endenumeration"]
old-location: wmi\iwbemclassobject_endenumeration.htm
tech.root: wmi
ms.assetid: a9fa8567-7504-4d59-a874-1dc7b2620a0b
ms.date: 12/05/2018
ms.keywords: EndEnumeration, EndEnumeration method [Windows Management Instrumentation], EndEnumeration method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],EndEnumeration method, IWbemClassObject.EndEnumeration, IWbemClassObject::EndEnumeration, _hmm_iwbemclassobject_endenumeration, wbemcli/IWbemClassObject::EndEnumeration, wmi.iwbemclassobject_endenumeration
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
 - IWbemClassObject::EndEnumeration
 - wbemcli/IWbemClassObject::EndEnumeration
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
 - IWbemClassObject.EndEnumeration
---

# IWbemClassObject::EndEnumeration


## -description

The 
<b>IWbemClassObject::EndEnumeration</b> method terminates an enumeration sequence started with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">IWbemClassObject::BeginEnumeration</a>. This call is not required, but it is recommended to developers because it releases resources associated with the enumeration. However, the resources are deallocated automatically when the next enumeration is started or the object is released.



## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">IWbemClassObject::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-next">IWbemClassObject::Next</a>
