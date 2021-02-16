---
UID: NF:wbemcli.IWbemContext.SetValue
title: IWbemContext::SetValue (wbemcli.h)
description: The IWbemContext::SetValue method creates or overwrites a named context value.
helpviewer_keywords: ["IWbemContext interface [Windows Management Instrumentation]","SetValue method","IWbemContext.SetValue","IWbemContext::SetValue","SetValue","SetValue method [Windows Management Instrumentation]","SetValue method [Windows Management Instrumentation]","IWbemContext interface","_hmm_iwbemcontext_setvalue","wbemcli/IWbemContext::SetValue","wmi.iwbemcontext_setvalue"]
old-location: wmi\iwbemcontext_setvalue.htm
tech.root: wmi
ms.assetid: 074d5ac7-aa86-44d8-99f9-959ef99a8004
ms.date: 12/05/2018
ms.keywords: IWbemContext interface [Windows Management Instrumentation],SetValue method, IWbemContext.SetValue, IWbemContext::SetValue, SetValue, SetValue method [Windows Management Instrumentation], SetValue method [Windows Management Instrumentation],IWbemContext interface, _hmm_iwbemcontext_setvalue, wbemcli/IWbemContext::SetValue, wmi.iwbemcontext_setvalue
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
 - IWbemContext::SetValue
 - wbemcli/IWbemContext::SetValue
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
 - IWbemContext.SetValue
---

# IWbemContext::SetValue


## -description

The 
<b>IWbemContext::SetValue</b> method creates or overwrites a named context value.

## -parameters

### -param wszName [in]

Cannot be <b>NULL</b>. It is a read-only pointer that  indicates the context value name. This value must be <b>null</b>-terminated.

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param pValue [in]

Must point to a valid <b>VARIANT</b>, which is treated as read-only. The value in the <b>VARIANT</b> becomes the named context value. An entire 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object can be stored as well as a simple value by enclosing it in a <b>VARIANT</b> that uses the <b>VT_UNKNOWN</b> type. The caller must execute <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the 
<b>IWbemClassObject</b> object by asking for <b>IID_IUnknown</b>, and by using the returned pointer in the <b>VARIANT</b>.

If <i>pValue</i> is to contain an embedded 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> object, the caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IWbemClassObject::QueryInterface</a> for <b>IID_IUnknown</b> and place the resulting pointer in the <b>VARIANT</b> by using a type of <b>VT_UNKNOWN</b>. The original embedded object is copied during the write operation, and so cannot be modified by the operation.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of a method call. The following list lists and describes the values contained in an <b>HRESULT</b>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemcontext-getvalue">IWbemContext::GetValue</a>