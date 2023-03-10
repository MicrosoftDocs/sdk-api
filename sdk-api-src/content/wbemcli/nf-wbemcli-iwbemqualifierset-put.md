---
UID: NF:wbemcli.IWbemQualifierSet.Put
title: IWbemQualifierSet::Put (wbemcli.h)
description: The IWbemQualifierSet::Put method writes the named qualifier and value. The new qualifier overwrites the previous value of the same name. If the qualifier does not exist, it is created.
helpviewer_keywords: ["IWbemQualifierSet interface [Windows Management Instrumentation]","Put method","IWbemQualifierSet.Put","IWbemQualifierSet::Put","Put","Put method [Windows Management Instrumentation]","Put method [Windows Management Instrumentation]","IWbemQualifierSet interface","WBEM_FLAVOR_AMENDED","WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS","WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE","WBEM_FLAVOR_NOT_OVERRIDABLE","WBEM_FLAVOR_OVERRIDABLE","_hmm_iwbemqualifierset_put","wbemcli/IWbemQualifierSet::Put","wmi.iwbemqualifierset_put"]
old-location: wmi\iwbemqualifierset_put.htm
tech.root: wmi
ms.assetid: ad602440-dc19-45cf-bf10-a30f514e00bb
ms.date: 12/05/2018
ms.keywords: IWbemQualifierSet interface [Windows Management Instrumentation],Put method, IWbemQualifierSet.Put, IWbemQualifierSet::Put, Put, Put method [Windows Management Instrumentation], Put method [Windows Management Instrumentation],IWbemQualifierSet interface, WBEM_FLAVOR_AMENDED, WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS, WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE, WBEM_FLAVOR_NOT_OVERRIDABLE, WBEM_FLAVOR_OVERRIDABLE, _hmm_iwbemqualifierset_put, wbemcli/IWbemQualifierSet::Put, wmi.iwbemqualifierset_put
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemQualifierSet::Put
 - wbemcli/IWbemQualifierSet::Put
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
api_name:
 - IWbemQualifierSet.Put
---

# IWbemQualifierSet::Put


## -description

The <b>IWbemQualifierSet::Put</b> method writes the named qualifier and value. The new qualifier overwrites the previous  value of the same name. If the qualifier does not exist, it is created.

Sometimes it is not possible to write the value of a qualifier, for example, if the qualifier is  propagated from another object. Typically, propagated qualifiers are read-only, but they can be overridden. For more information, see 
<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>.

When using the <a href="/windows/desktop/WmiSdk/standard-qualifiers">Key</a> qualifier, it is not necessary to specify any flavors or propagation rules.

The user may not create qualifiers with names that begin or end with an underscore (_). This is reserved for system classes and properties.

## -parameters

### -param wszName [in]

Name of the qualifier that is being written. The pointer is treated as read-only.

### -param pVal [in]

Cannot be <b>NULL</b>. This must point to a valid <b>VARIANT</b> that contains the qualifier value to be written. The pointer is treated as read-only. It is the caller's responsibility to call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> on this pointer after the value is not required.

Only variants and arrays of type <b>VT_I4</b>, <b>VT_R8</b>, <b>VT_BSTR</b>, <b>VT_BOOL</b> are supported.

### -param lFlavor [in]

Desired qualifier flavors for this qualifier.  The following list lists the appropriate constants for <i>lFlavor</i>. The default value is zero (0).



#### WBEM_FLAVOR_OVERRIDABLE (0 (0x0))

The qualifier value can be overridden in a derived class or an instance. This is the default. Using this constant is the same as using the <b>EnableOverride</b> flag.



#### WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE (1 (0x1))

The qualifier is propagated to instances. Using this constant is the same as using the <b>ToInstance</b> flag.



#### WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS (2 (0x2))

The qualifier is propagated to derived classes. Using this constant is the same as using the <b>ToSubClass</b> flag.



#### WBEM_FLAVOR_NOT_OVERRIDABLE (16 (0x10))

The qualifier value cannot be overridden in a derived class or an instance. Using this constant is the same as using the <b>DisableOverride</b> flag.



#### WBEM_FLAVOR_AMENDED (128 (0x80))

The qualifier is localized. Using this constant is the same as using the <b>Amended</b> flag.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>