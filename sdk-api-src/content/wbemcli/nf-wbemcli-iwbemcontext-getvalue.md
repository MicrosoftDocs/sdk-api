---
UID: NF:wbemcli.IWbemContext.GetValue
title: IWbemContext::GetValue (wbemcli.h)
description: The IWbemContext::GetValue method is used to retrieve a specific named context value by name.
helpviewer_keywords: ["GetValue","GetValue method [Windows Management Instrumentation]","GetValue method [Windows Management Instrumentation]","IWbemContext interface","IWbemContext interface [Windows Management Instrumentation]","GetValue method","IWbemContext.GetValue","IWbemContext::GetValue","_hmm_iwbemcontext_getvalue","wbemcli/IWbemContext::GetValue","wmi.iwbemcontext_getvalue"]
old-location: wmi\iwbemcontext_getvalue.htm
tech.root: wmi
ms.assetid: e11fff37-aeb7-41c5-8639-ca0a7a144263
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Windows Management Instrumentation], GetValue method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],GetValue method, IWbemContext.GetValue, IWbemContext::GetValue, _hmm_iwbemcontext_getvalue, wbemcli/IWbemContext::GetValue, wmi.iwbemcontext_getvalue
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
 - IWbemContext::GetValue
 - wbemcli/IWbemContext::GetValue
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
 - IWbemContext.GetValue
---

# IWbemContext::GetValue


## -description

The 
<b>IWbemContext::GetValue</b> method is used to retrieve a specific named context value by name.

## -parameters

### -param wszName [in]

Name for which the value is to be retrieved. This must point to a valid <b>BSTR</b>. The pointer is treated as read-only.

### -param lFlags [in]

Reserved. This parameter must be 0.

### -param pValue [out]

This parameter cannot be <b>NULL</b> and must point to an uninitialized <b>VARIANT</b>. If no error is returned, the <b>VARIANT</b> is initialized using <b>VariantInit</b>, and then set to contain the context value. The caller must call <b>VariantClear</b> on this pointer when the value is no longer required. If an error code is returned, the <b>VARIANT</b> pointed to by <i>pValue</i> is left unmodified.

It is possible that an entire 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object can be returned inside the <b>VARIANT</b>. If that is the case, then <b>VT_UNKNOWN</b> is the <b>VARIANT</b> type. The caller can take the <b>IUnknown</b> pointer and execute <b>QueryInterface</b> to obtain the 
<b>IWbemClassObject</b> pointer.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-setvalue">IWbemContext::SetValue</a>