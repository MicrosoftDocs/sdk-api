---
UID: NF:wbemcli.IEnumWbemClassObject.Reset
title: IEnumWbemClassObject::Reset method
author: windows-driver-content
description: The IEnumWbemClassObject::Reset method resets an enumeration sequence back to the beginning. Because CIM objects are dynamic, calling this method does not necessarily return the same list of objects that you obtained previously.
old-location: wmi\ienumwbemclassobject_reset.htm
old-project: WmiSdk
ms.assetid: 571b7067-676f-4e9e-9694-268ec10dc60b
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: IEnumWbemClassObject, IEnumWbemClassObject interface [Windows Management Instrumentation], Reset method, IEnumWbemClassObject::Reset, Reset method [Windows Management Instrumentation], Reset method [Windows Management Instrumentation], IEnumWbemClassObject interface, Reset,IEnumWbemClassObject.Reset, _hmm_ienumwbemclassobject_reset, wbemcli/IEnumWbemClassObject::Reset, wmi.ienumwbemclassobject_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fastprox.dll
api_name:
-	IEnumWbemClassObject.Reset
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWbemClassObject::Reset method


## -description


The 
<b>IEnumWbemClassObject::Reset</b> method resets an enumeration sequence back to the beginning. Because CIM objects are dynamic, calling this method does not necessarily return the same list of objects that you obtained previously.
<div class="alert"><b>Note</b>  This method fails if the enumerator was originally created with the <b>WBEM_FLAG_FORWARD_ONLY</b> option.</div><div> </div>

## -parameters






## -returns



The 
<b>Reset</b> method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



The COM-specific error codes may also be returned if the remote connection to the Windows Management is lost due to network problems.

You may see COM-specific error codes returned if network problems cause you to lose the remote connection to Windows Management.

If <b>WBEM_S_NO_ERROR</b> is not returned, you can call the COM function <b>GetErrorInfo</b> to get  more information about the error.



