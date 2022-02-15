---
UID: NF:wbemcli.IWbemQualifierSet.GetNames
title: IWbemQualifierSet::GetNames (wbemcli.h)
description: The IWbemQualifierSet::GetNames method retrieves the names of all of the qualifiers available from the current object or property. Alternately, depending on the filter value of IFlags, this method retrieves the names of certain qualifiers.
helpviewer_keywords: ["0 (Zero)","GetNames","GetNames method [Windows Management Instrumentation]","GetNames method [Windows Management Instrumentation]","IWbemQualifierSet interface","IWbemQualifierSet interface [Windows Management Instrumentation]","GetNames method","IWbemQualifierSet.GetNames","IWbemQualifierSet::GetNames","WBEM_FLAG_LOCAL_ONLY","WBEM_FLAG_PROPAGATED_ONLY","_hmm_iwbemqualifierset_getnames","wbemcli/IWbemQualifierSet::GetNames","wmi.iwbemqualifierset_getnames"]
old-location: wmi\iwbemqualifierset_getnames.htm
tech.root: wmi
ms.assetid: b1e7f6b2-a204-4e00-87eb-686bf8696082
ms.date: 12/05/2018
ms.keywords: 0 (Zero), GetNames, GetNames method [Windows Management Instrumentation], GetNames method [Windows Management Instrumentation],IWbemQualifierSet interface, IWbemQualifierSet interface [Windows Management Instrumentation],GetNames method, IWbemQualifierSet.GetNames, IWbemQualifierSet::GetNames, WBEM_FLAG_LOCAL_ONLY, WBEM_FLAG_PROPAGATED_ONLY, _hmm_iwbemqualifierset_getnames, wbemcli/IWbemQualifierSet::GetNames, wmi.iwbemqualifierset_getnames
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
 - IWbemQualifierSet::GetNames
 - wbemcli/IWbemQualifierSet::GetNames
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
 - IWbemQualifierSet.GetNames
---

# IWbemQualifierSet::GetNames


## -description

The 
<b>IWbemQualifierSet::GetNames</b> method retrieves the names of all of the qualifiers available from the current object or property. Alternately, depending on the filter value of <i>IFlags</i>, this method retrieves the names of certain qualifiers.

You can access these qualifiers by name, using 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-get">IWbemQualifierSet::Get</a> for each name. It is not an error for any given object to have zero qualifiers, so the number of strings in <i>pstrNames</i> on return can be 0, even though <b>WBEM_S_NO_ERROR</b> returns.

## -parameters

### -param lFlags [in]

One of the following constants.



#### 0 (Zero)

Return the names of all qualifiers.



#### WBEM_FLAG_LOCAL_ONLY

Return only the names of qualifiers specific to the current property or object. If the current qualifiers set refers to a property, return only the qualifiers specific to the property (including overrides), and not those qualifiers propagated from the class definition. If the current qualifiers set refers to an instance, return only instance-specific qualifier names. If the current qualifiers set refers to a class, return only qualifiers specific to the class being derived.



#### WBEM_FLAG_PROPAGATED_ONLY

Return only the names of qualifiers propagated from another object. For example, if the current qualifier set refers to a property, return only the qualifiers propagated to this property from the class definition, and not those from the property itself. If the current qualifier set refers to an instance, return only those qualifiers propagated from the class definition. If the current qualifier set refers to a class, return only those qualifier names inherited from the parent classes.

### -param pNames [out]

A new <b>SAFEARRAY</b> is created that contains the requested names.

In all cases where no error is returned, a new array is created and <i>pstrNames</i> is set to point to it. This occurs even though the resulting array has zero elements. On error, a new <b>SAFEARRAY</b> is not returned.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

For an example of using <b>SAFEARRAY</b>s of <b>BSTR</b>s, see 
<a href="/windows/desktop/WmiSdk/retrieving-part-of-an-instance">Retrieving Part of a WMI Instance</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-beginenumeration">IWbemQualifierSet::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-get">IWbemQualifierSet::Get</a>