---
UID: NF:wbemcli.IWbemQualifierSet.Get
title: IWbemQualifierSet::Get (wbemcli.h)
description: The IWbemQualifierSet::Get method gets the specified named qualifier, if found.
helpviewer_keywords: ["Get","Get method [Windows Management Instrumentation]","Get method [Windows Management Instrumentation]","IWbemQualifierSet interface","IWbemQualifierSet interface [Windows Management Instrumentation]","Get method","IWbemQualifierSet.Get","IWbemQualifierSet::Get","_hmm_iwbemqualifierset_get","wbemcli/IWbemQualifierSet::Get","wmi.iwbemqualifierset_get"]
old-location: wmi\iwbemqualifierset_get.htm
tech.root: wmi
ms.assetid: f4663cd1-0dc9-4021-918e-d5eda1648429
ms.date: 12/05/2018
ms.keywords: Get, Get method [Windows Management Instrumentation], Get method [Windows Management Instrumentation],IWbemQualifierSet interface, IWbemQualifierSet interface [Windows Management Instrumentation],Get method, IWbemQualifierSet.Get, IWbemQualifierSet::Get, _hmm_iwbemqualifierset_get, wbemcli/IWbemQualifierSet::Get, wmi.iwbemqualifierset_get
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
 - IWbemQualifierSet::Get
 - wbemcli/IWbemQualifierSet::Get
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
 - IWbemQualifierSet.Get
---

# IWbemQualifierSet::Get


## -description

The <b>IWbemQualifierSet::Get</b> method gets the specified named qualifier, if found.

## -parameters

### -param wszName [in]

Name of the qualifier for which the value is being requested. The pointer is treated as read-only.

### -param lFlags [in]

Reserved. This parameter must be 0.

### -param pVal [out]

When successful, <b>VARIANT</b> is assigned to the correct type and value for the qualifier. <b>VariantInit</b> is called on this <b>VARIANT</b>.

It is the responsibility of the caller to call <b>VariantClear</b> on the pointer when the value is no longer required. If there is an error code, the <b>VARIANT</b> pointed to by <i>pVal</i> is not modified.

If this parameter is <b>NULL</b>, the parameter is ignored.

### -param plFlavor [out]

Can be <b>NULL</b>. If not <b>NULL</b>, this must point to a <b>LONG</b> that receives the qualifier flavor bits for the requested qualifier. For more information, see 
<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a> and <a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_flavor_type">WBEM_FLAVOR_TYPE</a>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a>