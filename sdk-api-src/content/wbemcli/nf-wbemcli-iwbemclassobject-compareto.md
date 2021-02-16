---
UID: NF:wbemcli.IWbemClassObject.CompareTo
title: IWbemClassObject::CompareTo (wbemcli.h)
description: The IWbemClassObject::CompareTo method compares an object to another Windows Management object. Note that there are certain constraints in this comparison process.
helpviewer_keywords: ["CompareTo","CompareTo method [Windows Management Instrumentation]","CompareTo method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","CompareTo method","IWbemClassObject.CompareTo","IWbemClassObject::CompareTo","WBEM_FLAG_IGNORE_CASE","WBEM_FLAG_IGNORE_CLASS","WBEM_FLAG_IGNORE_DEFAULT_VALUES","WBEM_FLAG_IGNORE_FLAVOR","WBEM_FLAG_IGNORE_OBJECT_SOURCE","WBEM_FLAG_IGNORE_QUALIFIERS","_hmm_iwbemclassobject_compareto","wbemcli/IWbemClassObject::CompareTo","wmi.iwbemclassobject_compareto"]
old-location: wmi\iwbemclassobject_compareto.htm
tech.root: wmi
ms.assetid: 246e5c2e-8d89-4ab5-b9ae-21a41eefa2e2
ms.date: 12/05/2018
ms.keywords: CompareTo, CompareTo method [Windows Management Instrumentation], CompareTo method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],CompareTo method, IWbemClassObject.CompareTo, IWbemClassObject::CompareTo, WBEM_FLAG_IGNORE_CASE, WBEM_FLAG_IGNORE_CLASS, WBEM_FLAG_IGNORE_DEFAULT_VALUES, WBEM_FLAG_IGNORE_FLAVOR, WBEM_FLAG_IGNORE_OBJECT_SOURCE, WBEM_FLAG_IGNORE_QUALIFIERS, _hmm_iwbemclassobject_compareto, wbemcli/IWbemClassObject::CompareTo, wmi.iwbemclassobject_compareto
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
 - IWbemClassObject::CompareTo
 - wbemcli/IWbemClassObject::CompareTo
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
 - IWbemClassObject.CompareTo
---

# IWbemClassObject::CompareTo


## -description

The <b>IWbemClassObject::CompareTo</b> method compares an object to another Windows Management object. Note that there are certain constraints in this comparison process.

## -parameters

### -param lFlags [in]

Specifies the object characteristics to consider in comparison to another object. It can be <b>WBEM_COMPARISON_INCLUDE_ALL</b> to consider all features, or any combination of these flags.



#### WBEM_FLAG_IGNORE_OBJECT_SOURCE

Ignore the source of the objects, namely the server and the namespace they came from, in comparison to other objects.



#### WBEM_FLAG_IGNORE_QUALIFIERS

Ignore all qualifiers (including <b>Key</b> and <b>Dynamic</b>) in comparison.



#### WBEM_FLAG_IGNORE_DEFAULT_VALUES

Ignore default values of properties. This flag is only meaningful when comparing classes.



#### WBEM_FLAG_IGNORE_FLAVOR

Ignore qualifier flavors. This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions (for more information, see 
<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>).



#### WBEM_FLAG_IGNORE_CASE

Compare string values in a case-insensitive manner. This applies both to strings and to qualifier values. Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.



#### WBEM_FLAG_IGNORE_CLASS

Assume that the objects being compared are instances of the same class. Consequently, this flag compares instance-related information only. Use this flag to optimize performance. If the objects are not of the same class, the results are undefined.

### -param pCompareTo [in]

Object in comparison. This pointer must point to a valid 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> instance. It cannot be <b>NULL</b>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_comparison_flag">WBEM_COMPARISON_FLAG</a>