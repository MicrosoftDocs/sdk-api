---
UID: NF:methodco.MethodContext.GetStatusObject
title: MethodContext::GetStatusObject (methodco.h)
description: The GetStatusObject method gets an internal pointer to IWbemClassObject information. WMI does not implement any functionality based on the pointer.
helpviewer_keywords: ["?GetStatusObject@MethodContext@@QAEPAUIWbemClassObject@@XZ","GetStatusObject","GetStatusObject method [Windows Management Instrumentation]","GetStatusObject method [Windows Management Instrumentation]","MethodContext interface","MethodContext interface [Windows Management Instrumentation]","GetStatusObject method","MethodContext.GetStatusObject","MethodContext::GetStatusObject","methodco/MethodContext::GetStatusObject","wmi.methodcontext_getstatusobject"]
old-location: wmi\methodcontext_getstatusobject.htm
tech.root: wmi
ms.assetid: dc68eddb-7991-42bd-bc0e-4f5d890ca468
ms.date: 12/05/2018
ms.keywords: ?GetStatusObject@MethodContext@@QAEPAUIWbemClassObject@@XZ, GetStatusObject, GetStatusObject method [Windows Management Instrumentation], GetStatusObject method [Windows Management Instrumentation],MethodContext interface, MethodContext interface [Windows Management Instrumentation],GetStatusObject method, MethodContext.GetStatusObject, MethodContext::GetStatusObject, methodco/MethodContext::GetStatusObject, wmi.methodcontext_getstatusobject
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
 - MethodContext::GetStatusObject
 - methodco/MethodContext::GetStatusObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - framedynos.dll
api_name:
 - MethodContext.GetStatusObject
 - ?GetStatusObject@MethodContext@@QAEPAUIWbemClassObject@@XZ
---

## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/methodco/nl-methodco-methodcontext">MethodContext</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetStatusObject</b> method gets an internal pointer to <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.



## -returns

Type: **[IWbemClassObject](../wbemcli/nn-wbemcli-iwbemclassobject.md)\***

A pointer to the **IWbemClassObject** information.

## -see-also

<a href="/windows/desktop/api/methodco/nl-methodco-methodcontext">MethodContext</a>
