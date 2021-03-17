---
UID: NF:wbemcli.IWbemClassObject.BeginEnumeration
title: IWbemClassObject::BeginEnumeration (wbemcli.h)
description: Resets an enumeration back to the beginning of the enumeration.
helpviewer_keywords: ["BeginEnumeration","BeginEnumeration method [Windows Management Instrumentation]","BeginEnumeration method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","BeginEnumeration method","IWbemClassObject.BeginEnumeration","IWbemClassObject::BeginEnumeration","_hmm_iwbemclassobject_beginenumeration","wbemcli/IWbemClassObject::BeginEnumeration","wmi.iwbemclassobject_beginenumeration"]
old-location: wmi\iwbemclassobject_beginenumeration.htm
tech.root: wmi
ms.assetid: c7ece530-5309-4f0d-9096-73d01b4a7fde
ms.date: 12/05/2018
ms.keywords: BeginEnumeration, BeginEnumeration method [Windows Management Instrumentation], BeginEnumeration method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],BeginEnumeration method, IWbemClassObject.BeginEnumeration, IWbemClassObject::BeginEnumeration, _hmm_iwbemclassobject_beginenumeration, wbemcli/IWbemClassObject::BeginEnumeration, wmi.iwbemclassobject_beginenumeration
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
 - IWbemClassObject::BeginEnumeration
 - wbemcli/IWbemClassObject::BeginEnumeration
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
 - IWbemClassObject.BeginEnumeration
---

# IWbemClassObject::BeginEnumeration


## -description

The 
<b>IWbemClassObject::BeginEnumeration</b> method resets an enumeration back to the beginning of the enumeration. The caller must call this method prior to the first call to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-next">IWbemClassObject::Next</a> to enumerate all of the properties on an object. The order in which properties are enumerated is guaranteed to be invariant for a given instance of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>.

## -parameters

### -param lEnumFlags [in]

Combination of flags described in Remarks.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

You can control the properties included in the enumeration by specifying a combination of the following flags. You can combine one flag from each group with any flag from any other group. However, flags from the same group are mutually exclusive.

GROUP 1



GROUP 2

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endenumeration">IWbemClassObject::EndEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-next">IWbemClassObject::Next</a>



<a href="/windows/desktop/WmiSdk/wmi-system-properties">WMI System Properties</a>