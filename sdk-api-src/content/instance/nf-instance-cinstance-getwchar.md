---
UID: NF:instance.CInstance.GetWCHAR
title: CInstance::GetWCHAR (instance.h)
description: The GetWCHAR method retrieves a WCHAR string property.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","GetWCHAR method","CInstance.GetWCHAR","CInstance::GetWCHAR","GetWCHAR","GetWCHAR method [Windows Management Instrumentation]","GetWCHAR method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getwchar","instance/CInstance::GetWCHAR","wmi.cinstance_getwchar"]
old-location: wmi\cinstance_getwchar.htm
tech.root: wmi
ms.assetid: 1c2f3dfc-aa84-4dff-a25b-b8f2ec3afa74
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetWCHAR method, CInstance.GetWCHAR, CInstance::GetWCHAR, GetWCHAR, GetWCHAR method [Windows Management Instrumentation], GetWCHAR method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getwchar, instance/CInstance::GetWCHAR, wmi.cinstance_getwchar
req.header: instance.h
req.include-header: FwCommon.h
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CInstance::GetWCHAR
 - instance/CInstance::GetWCHAR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-crt-stdio-l1-1-0.dll
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetWCHAR
---

# CInstance::GetWCHAR


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetWCHAR</b> method retrieves a <b>WCHAR</b> string property.

## -parameters

### -param name

Name of the <b>WCHAR</b> string property retrieved.

### -param pW

Buffer that receives the <b>WCHAR</b> string property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a type that is <b>WCHAR</b> string-compatible or a property that does not exist. More information is available in the log file, Framework.log.

## -remarks

It is the responsibility of the implementer to free the memory occupied by the <b>WCHAR</b> string:


```cpp
    free(pw);
```


Use <b>free</b> rather than <b>delete</b> because the provider framework allocates the string using <b>malloc</b> and does not use the <b>new</b> operator.