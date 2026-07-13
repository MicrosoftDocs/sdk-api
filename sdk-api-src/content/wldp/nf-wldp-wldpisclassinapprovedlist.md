---
UID: NF:wldp.WldpIsClassInApprovedList
tech.root: security
title: WldpIsClassInApprovedList
ms.date: 08/23/2022
targetos: Windows
description: Calls the library to validate if a particular CLSID is safe to be called.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: wldp.dll
req.header: wldp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: wldp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wldp.dll
api_name:
 - WldpIsClassInApprovedList
f1_keywords:
 - WldpIsClassInApprovedList
 - wldp/WldpIsClassInApprovedList
dev_langs:
 - c++
helpviewer_keywords:
 - WldpIsClassInApprovedList
---

## -description

Calls the library to validate if a particular **CLSID** is safe to be called. The function has no associated import library. You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.

## -parameters

### -param classID

The COM class ID to check for approval.

### -param hostInformation

A [**WLDP\_HOST\_INFORMATION**](ns-wldp-wldp_host_information.md) structure identifying the host to be evaluated.

### -param isApproved

On successful completion, contains **TRUE** if the class ID is approved; otherwise, **FALSE**.

### -param optionalFlags

This parameter is reserved and must be set to zero.

## -returns

This method returns **S\_OK** if successful or a failure code otherwise.

## -remarks

## -see-also

