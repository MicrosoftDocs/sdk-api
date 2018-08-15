---
UID: NF:wbemcli.IWbemQualifierSet.Next
title: IWbemQualifierSet::Next
author: windows-sdk-content
description: The IWbemQualifierSet::Next method retrieves the next qualifier in an enumeration that started with IWbemQualifierSet::BeginEnumeration.
old-location: wmi\iwbemqualifierset_next.htm
old-project: WmiSdk
ms.assetid: 76afa293-1bd9-442b-bc9b-2247459bd49c
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IWbemQualifierSet interface [Windows Management Instrumentation],Next method, IWbemQualifierSet.Next, IWbemQualifierSet::Next, Next, Next method [Windows Management Instrumentation], Next method [Windows Management Instrumentation],IWbemQualifierSet interface, _hmm_iwbemqualifierset_next, wbemcli/IWbemQualifierSet::Next, wmi.iwbemqualifierset_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
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
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemQualifierSet::Next


## -description


The <b>IWbemQualifierSet::Next</b> method retrieves the next qualifier in an enumeration that started with 
<a href="https://msdn.microsoft.com/57fa60d1-54d2-412d-b39b-c35dfd709d0c">IWbemQualifierSet::BeginEnumeration</a>. This method is called repeatedly to enumerate all the qualifiers until <b>WBEM_S_NO_MORE_DATA</b> returns. To terminate the enumeration early, call 
<a href="https://msdn.microsoft.com/317409e9-b098-404b-bc09-78b5b5ae7fc7">IWbemQualifierSet::EndEnumeration</a>.

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
<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a> and <a href="https://msdn.microsoft.com/A21ED0FD-1207-42B6-92AE-6080D0E98771">WBEM_FLAVOR_TYPE</a>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/57fa60d1-54d2-412d-b39b-c35dfd709d0c">IWbemQualifierSet::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/317409e9-b098-404b-bc09-78b5b5ae7fc7">IWbemQualifierSet::EndEnumeration</a>



<a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a>
 

 

