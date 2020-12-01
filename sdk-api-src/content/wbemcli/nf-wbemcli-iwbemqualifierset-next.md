---
UID: NF:wbemcli.IWbemQualifierSet.Next
title: IWbemQualifierSet::Next (wbemcli.h)
description: The IWbemQualifierSet::Next method retrieves the next qualifier in an enumeration that started with IWbemQualifierSet::BeginEnumeration.
helpviewer_keywords: ["IWbemQualifierSet interface [Windows Management Instrumentation]","Next method","IWbemQualifierSet.Next","IWbemQualifierSet::Next","Next","Next method [Windows Management Instrumentation]","Next method [Windows Management Instrumentation]","IWbemQualifierSet interface","_hmm_iwbemqualifierset_next","wbemcli/IWbemQualifierSet::Next","wmi.iwbemqualifierset_next"]
old-location: wmi\iwbemqualifierset_next.htm
tech.root: wmi
ms.assetid: 76afa293-1bd9-442b-bc9b-2247459bd49c
ms.date: 12/05/2018
ms.keywords: IWbemQualifierSet interface [Windows Management Instrumentation],Next method, IWbemQualifierSet.Next, IWbemQualifierSet::Next, Next, Next method [Windows Management Instrumentation], Next method [Windows Management Instrumentation],IWbemQualifierSet interface, _hmm_iwbemqualifierset_next, wbemcli/IWbemQualifierSet::Next, wmi.iwbemqualifierset_next
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
 - IWbemQualifierSet::Next
 - wbemcli/IWbemQualifierSet::Next
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
 - IWbemQualifierSet.Next
---

# IWbemQualifierSet::Next


## -description

The <b>IWbemQualifierSet::Next</b> method retrieves the next qualifier in an enumeration that started with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-beginenumeration">IWbemQualifierSet::BeginEnumeration</a>. This method is called repeatedly to enumerate all the qualifiers until <b>WBEM_S_NO_MORE_DATA</b> returns. To terminate the enumeration early, call 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-endenumeration">IWbemQualifierSet::EndEnumeration</a>.

The order of the qualifiers returned during the enumeration is not defined.

## -parameters

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param pstrName [out]

This parameter receives the name of the qualifier. A new <b>BSTR</b> is always allocated whenever <b>WBEM_S_NO_ERROR</b> returns.

If <i>pstrName</i> is <b>NULL</b>, it is ignored; otherwise, the caller must ensure that this parameter does not point to a valid <b>BSTR</b> on entry, or else there will be a memory leak. Also, the caller must remember to call <b>SysFreeString</b> on the returned string when it is no longer required.

### -param pVal [out]

This parameter receives the value for the qualifier. <b>VariantInit</b> is called on the <b>VARIANT</b> by this method. The caller must call <b>VariantClear</b> on this pointer when the value is no longer required. If an error code is returned, the <b>VARIANT</b> pointed to by <i>pVal</i> is left unmodified. This parameter is ignored if set to <b>NULL</b>.

### -param plFlavor [out]

If not <b>NULL</b>, the value pointed to is set to the qualifier flavor. For more information, see 
<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a> and <a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_flavor_type">WBEM_FLAVOR_TYPE</a>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-beginenumeration">IWbemQualifierSet::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-endenumeration">IWbemQualifierSet::EndEnumeration</a>



<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>