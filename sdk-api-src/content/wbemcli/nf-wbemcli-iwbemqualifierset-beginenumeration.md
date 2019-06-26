---
UID: NF:wbemcli.IWbemQualifierSet.BeginEnumeration
title: IWbemQualifierSet::BeginEnumeration (wbemcli.h)
author: windows-sdk-content
description: The IWbemQualifierSet::BeginEnumeration method resets before there is an enumeration of all the qualifiers in the object.
old-location: wmi\iwbemqualifierset_beginenumeration.htm
tech.root: WmiSdk
ms.assetid: 57fa60d1-54d2-412d-b39b-c35dfd709d0c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0 (Zero), BeginEnumeration, BeginEnumeration method [Windows Management Instrumentation], BeginEnumeration method [Windows Management Instrumentation],IWbemQualifierSet interface, IWbemQualifierSet interface [Windows Management Instrumentation],BeginEnumeration method, IWbemQualifierSet.BeginEnumeration, IWbemQualifierSet::BeginEnumeration, WBEM_FLAG_LOCAL_ONLY, WBEM_FLAG_PROPAGATED_ONLY, _hmm_iwbemqualifierset_beginenumeration, wbemcli/IWbemQualifierSet::BeginEnumeration, wmi.iwbemqualifierset_beginenumeration
ms.topic: method
f1_keywords: 
 - "wbemcli/IWbemQualifierSet.BeginEnumeration"
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
 - IWbemQualifierSet.BeginEnumeration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemQualifierSet::BeginEnumeration


## -description


The 
<b>IWbemQualifierSet::BeginEnumeration</b> method resets before there is an enumeration of all the qualifiers in the object. To enumerate all of the qualifiers on an object, this method must be called before the first call to 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-next">IWbemQualifierSet::Next</a>. The order in which qualifiers are enumerated is guaranteed to be invariant for a given instance of 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a>.


## -parameters




### -param lFlags [in]

Specifies the qualifiers to include in the enumeration. It must be one of the following constants.



#### 0 (Zero)

Return the names of all qualifiers.



#### WBEM_FLAG_LOCAL_ONLY

Return only the names of qualifiers specific to the current property or object. If the current qualifiers set refers to a property, return only the qualifiers specific to the property (including overrides), and not those qualifiers propagated from the class definition. If the current qualifiers set refers to an instance, return only instance-specific qualifier names. If the current qualifiers set refers to a class, return only qualifiers specific to the class being derived.



#### WBEM_FLAG_PROPAGATED_ONLY

Return only the names of qualifiers propagated from another object. For example, if the current qualifier set refers to a property, return only the qualifiers propagated to this property from the class definition, and not those from the property itself. If the current qualifier set refers to an instance, only return those qualifiers propagated from the class definition. If the current qualifier set refers to a class, only return those qualifier names inherited from the parent classes.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-next">IWbemQualifierSet::Next</a>
 

 

