---
UID: NF:wbemcli.IWbemContext.Next
title: IWbemContext::Next (wbemcli.h)
description: The IWbemContext::Next method retrieves the next value in an enumeration of all context values beginning with IWbemContext::BeginEnumeration.
helpviewer_keywords: ["IWbemContext interface [Windows Management Instrumentation]","Next method","IWbemContext.Next","IWbemContext::Next","Next","Next method [Windows Management Instrumentation]","Next method [Windows Management Instrumentation]","IWbemContext interface","_hmm_iwbemcontext_next","wbemcli/IWbemContext::Next","wmi.iwbemcontext_next"]
old-location: wmi\iwbemcontext_next.htm
tech.root: wmi
ms.assetid: e316564c-a739-472b-b7a8-8acbf71e1c58
ms.date: 12/05/2018
ms.keywords: IWbemContext interface [Windows Management Instrumentation],Next method, IWbemContext.Next, IWbemContext::Next, Next, Next method [Windows Management Instrumentation], Next method [Windows Management Instrumentation],IWbemContext interface, _hmm_iwbemcontext_next, wbemcli/IWbemContext::Next, wmi.iwbemcontext_next
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
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemContext::Next
 - wbemcli/IWbemContext::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipjobj.dll
api_name:
 - IWbemContext.Next
---

# IWbemContext::Next


## -description

The 
<b>IWbemContext::Next</b> method retrieves the next value in an enumeration of all context values beginning with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-beginenumeration">IWbemContext::BeginEnumeration</a>.

## -parameters

### -param lFlags [in]

Reserved. This parameter must be 0.

### -param pstrName [out]

This parameter cannot be <b>NULL</b>. The pointer must not point to an active <b>BSTR</b> on entry, and ideally it should be set to point to <b>NULL</b>. If no error code is returned, it is set to point to a newly allocated <b>BSTR</b> containing the context value name.

The caller must call <b>SysFreeString</b> on the returned string when it is no longer required. If <b>WBEM_S_NO_MORE_DATA</b> returns, <i>pstrName</i> is set to point to <b>NULL</b>, in which case <b>SysFreeString</b> should not be called. Note that if <i>pstrName</i> points to a valid <b>BSTR</b> on entry, this <b>BSTR</b> is not freed, and a memory leak occurs.

### -param pValue [out]

This parameter cannot be <b>NULL</b>, and it must point to an empty or uninitialized <b>VARIANT</b>. If no error is returned, the <b>VARIANT</b> is initialized using <b>VariantInit</b>, and then set to contain the context value. The caller must call <b>VariantClear</b> on this pointer when the value is no longer required. If an error code is returned, the <b>VARIANT</b> pointed to by <i>pValue</i> is left unmodified.

If <b>WBEM_S_NO_MORE_DATA</b> returns, this parameter is set to point to a <b>VARIANT</b> of type <b>VT_NULL</b>.

It is possible that an entire 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object may be returned inside the <b>VARIANT</b>. If that is the case, then <b>VT_UNKNOWN</b> is the <b>VARIANT</b> type. The caller can take the <b>IUnknown</b> pointer and execute <b>QueryInterface</b> to obtain the 
<b>IWbemClassObject</b> pointer.

<div class="alert"><b>Note</b>  At the end of the enumeration, <b>WBEM_S_NO_MORE_DATA</b> is returned. The returned <b>VARIANT</b> is of type <b>VT_NULL</b>, and the returned <i>pstrName</i> is <b>NULL</b>.</div>
<div> </div>

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-beginenumeration">IWbemContext::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-endenumeration">IWbemContext::EndEnumeration</a>