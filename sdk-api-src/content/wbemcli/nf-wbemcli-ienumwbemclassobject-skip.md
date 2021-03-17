---
UID: NF:wbemcli.IEnumWbemClassObject.Skip
title: IEnumWbemClassObject::Skip (wbemcli.h)
description: You can use the IEnumWbemClassObject::Skip method to move the current position in an enumeration ahead by a specified number of objects. Also, this affects subsequent calls to NextAsync, but it does not affect pending deliveries begun with NextAsync.
helpviewer_keywords: ["IEnumWbemClassObject interface [Windows Management Instrumentation]","Skip method","IEnumWbemClassObject.Skip","IEnumWbemClassObject::Skip","Skip","Skip method [Windows Management Instrumentation]","Skip method [Windows Management Instrumentation]","IEnumWbemClassObject interface","_hmm_ienumwbemclassobject_skip","wbemcli/IEnumWbemClassObject::Skip","wmi.ienumwbemclassobject_skip"]
old-location: wmi\ienumwbemclassobject_skip.htm
tech.root: wmi
ms.assetid: 9579086c-cd45-4b3c-bd43-de0b89745b02
ms.date: 12/05/2018
ms.keywords: IEnumWbemClassObject interface [Windows Management Instrumentation],Skip method, IEnumWbemClassObject.Skip, IEnumWbemClassObject::Skip, Skip, Skip method [Windows Management Instrumentation], Skip method [Windows Management Instrumentation],IEnumWbemClassObject interface, _hmm_ienumwbemclassobject_skip, wbemcli/IEnumWbemClassObject::Skip, wmi.ienumwbemclassobject_skip
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
req.dll: Fastprox.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumWbemClassObject::Skip
 - wbemcli/IEnumWbemClassObject::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IEnumWbemClassObject.Skip
---

# IEnumWbemClassObject::Skip


## -description

You can use the 
<b>IEnumWbemClassObject::Skip</b> method to move the current position in an enumeration ahead by a specified number of objects. Also, this affects subsequent calls to 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync">NextAsync</a>, but it does not affect pending deliveries begun with 
<b>NextAsync</b>.

## -parameters

### -param lTimeout [in]

Maximum amount of time in milliseconds that the call to 
<b>Skip</b> blocks before returning. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the operation succeeds. If 
<b>Skip</b> cannot complete the operation before the <i>lTimeout</i> value expires, the call returns <b>WBEM_S_TIMEDOUT</b>.

### -param nCount [in]

Number of objects to skip. If this parameter is greater than the number of objects left to enumerate, then this call skips to the end of the enumeration and <b>WBEM_S_FALSE</b> is returned.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.