---
UID: NF:wldp.WldpIsDynamicCodePolicyEnabled
tech.root: security
title: WldpIsDynamicCodePolicyEnabled
ms.date: 08/23/2022
targetos: Windows
description: Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.
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
req.target-min-winverclnt: Windows 10, version 1803
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
 - WldpIsDynamicCodePolicyEnabled
f1_keywords:
 - WldpIsDynamicCodePolicyEnabled
 - wldp/WldpIsDynamicCodePolicyEnabled
dev_langs:
 - c++
helpviewer_keywords:
 - WldpIsDynamicCodePolicyEnabled
---

## -description

Retrieves a value that describes the Device Guard policy enforcement status for .NET dynamic code.

## -parameters

### -param isEnabled

On success, returns **true** if the Device Guard policy enforces .NET Dynamic Code policy; otherwise, returns **false**.

## -returns

This method returns **S\_OK** if successful or a failure code otherwise.

## -remarks

Dynamic code refers to .NET CRL dynamically-generated code.

## -see-also

