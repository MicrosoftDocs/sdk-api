---
UID: NF:wbemcli.IEnumWbemClassObject.Skip
title: IEnumWbemClassObject::Skip method
author: windows-driver-content
description: You can use the IEnumWbemClassObject::Skip method to move the current position in an enumeration ahead by a specified number of objects. Also, this affects subsequent calls to NextAsync, but it does not affect pending deliveries begun with NextAsync.
old-location: wmi\ienumwbemclassobject_skip.htm
old-project: WmiSdk
ms.assetid: 9579086c-cd45-4b3c-bd43-de0b89745b02
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IEnumWbemClassObject, IEnumWbemClassObject interface [Windows Management Instrumentation], Skip method, IEnumWbemClassObject::Skip, Skip method [Windows Management Instrumentation], Skip method [Windows Management Instrumentation], IEnumWbemClassObject interface, Skip,IEnumWbemClassObject.Skip, _hmm_ienumwbemclassobject_skip, wbemcli/IEnumWbemClassObject::Skip, wmi.ienumwbemclassobject_skip
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
-	IEnumWbemClassObject.Skip
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWbemClassObject::Skip method


## -description


You can use the 
<b>IEnumWbemClassObject::Skip</b> method to move the current position in an enumeration ahead by a specified number of objects. Also, this affects subsequent calls to 
<a href="https://msdn.microsoft.com/1ff82982-a2d7-4618-8488-9e4b7628012d">NextAsync</a>, but it does not affect pending deliveries begun with 
<b>NextAsync</b>.


## -parameters




### -param lTimeout




### -param nCount






#### - UCount [in]

Number of objects to skip. If this parameter is greater than the number of objects left to enumerate, then this call skips to the end of the enumeration and <b>WBEM_S_FALSE</b> is returned.


#### - lTimeOut [in]

Maximum amount of time in milliseconds that the call to 
<b>Skip</b> blocks before returning. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the operation succeeds. If 
<b>Skip</b> cannot complete the operation before the <i>lTimeout</i> value expires, the call returns <b>WBEM_S_TIMEDOUT</b>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.



