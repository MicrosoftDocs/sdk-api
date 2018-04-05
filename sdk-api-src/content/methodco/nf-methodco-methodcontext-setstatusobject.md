---
UID: NF:methodco.MethodContext.SetStatusObject
title: MethodContext::SetStatusObject method
author: windows-driver-content
description: The SetStatusObject method sets an internal pointer to IWbemClassObject information. WMI does not implement any functionality based on the pointer.
old-location: wmi\methodcontext_setstatusobject.htm
old-project: WmiSdk
ms.assetid: 5fe1f1af-61a9-490b-95e0-c3a3efe2392d
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: "?SetStatusObject@MethodContext@@QAE_NPAUIWbemClassObject@@@Z, ?SetStatusObject@MethodContext@@QEAA_NPEAUIWbemClassObject@@@Z, MethodContext, MethodContext interface [Windows Management Instrumentation], SetStatusObject method, MethodContext::SetStatusObject, SetStatusObject method [Windows Management Instrumentation], SetStatusObject method [Windows Management Instrumentation], MethodContext interface, SetStatusObject,MethodContext.SetStatusObject, methodco/MethodContext::SetStatusObject, wmi.methodcontext_setstatusobject"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MethodCo.h
api_name:
-	MethodContext.SetStatusObject
-	?SetStatusObject@MethodContext@@QAE_NPAUIWbemClassObject@@@Z
-	?SetStatusObject@MethodContext@@QEAA_NPEAUIWbemClassObject@@@Z
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MethodContext::SetStatusObject method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aea20c9d-4042-426a-abdf-51ebddf017aa">MethodContext</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetStatusObject</b> method sets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.


## -parameters




### -param pObj

A pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information.


## -returns



<b>TRUE</b> if the call method call was successful. <b>FALSE</b> if the object has already been set.




## -see-also




<a href="https://msdn.microsoft.com/aea20c9d-4042-426a-abdf-51ebddf017aa">MethodContext</a>
 

 

