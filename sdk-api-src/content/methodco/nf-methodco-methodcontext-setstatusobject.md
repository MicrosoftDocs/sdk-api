---
UID: NF:methodco.MethodContext.SetStatusObject
title: MethodContext::SetStatusObject (methodco.h)
description: The SetStatusObject method sets an internal pointer to IWbemClassObject information. WMI does not implement any functionality based on the pointer.
helpviewer_keywords: ["?SetStatusObject@MethodContext@@QAE_NPAUIWbemClassObject@@@Z","?SetStatusObject@MethodContext@@QEAA_NPEAUIWbemClassObject@@@Z","MethodContext interface [Windows Management Instrumentation]","SetStatusObject method","MethodContext.SetStatusObject","MethodContext::SetStatusObject","SetStatusObject","SetStatusObject method [Windows Management Instrumentation]","SetStatusObject method [Windows Management Instrumentation]","MethodContext interface","methodco/MethodContext::SetStatusObject","wmi.methodcontext_setstatusobject"]
old-location: wmi\methodcontext_setstatusobject.htm
tech.root: wmi
ms.assetid: 5fe1f1af-61a9-490b-95e0-c3a3efe2392d
ms.date: 12/05/2018
ms.keywords: ?SetStatusObject@MethodContext@@QAE_NPAUIWbemClassObject@@@Z, ?SetStatusObject@MethodContext@@QEAA_NPEAUIWbemClassObject@@@Z, MethodContext interface [Windows Management Instrumentation],SetStatusObject method, MethodContext.SetStatusObject, MethodContext::SetStatusObject, SetStatusObject, SetStatusObject method [Windows Management Instrumentation], SetStatusObject method [Windows Management Instrumentation],MethodContext interface, methodco/MethodContext::SetStatusObject, wmi.methodcontext_setstatusobject
req.header: methodco.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MethodContext::SetStatusObject
 - methodco/MethodContext::SetStatusObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MethodCo.h
api_name:
 - MethodContext.SetStatusObject
 - ?SetStatusObject@MethodContext@@QAE_NPAUIWbemClassObject@@@Z
 - ?SetStatusObject@MethodContext@@QEAA_NPEAUIWbemClassObject@@@Z
---

# MethodContext::SetStatusObject


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/methodco/nl-methodco-methodcontext">MethodContext</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetStatusObject</b> method sets an internal pointer to <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

## -parameters

### -param pObj

A pointer to <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> information.

## -returns

<b>TRUE</b> if the call method call was successful. <b>FALSE</b> if the object has already been set.

## -see-also

<a href="/windows/desktop/api/methodco/nl-methodco-methodcontext">MethodContext</a>