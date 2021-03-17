---
UID: NF:instance.CInstance.GetDOUBLE
title: CInstance::GetDOUBLE (instance.h)
description: The GetDOUBLE method retrieves a DOUBLE property.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","GetDOUBLE method","CInstance.GetDOUBLE","CInstance::GetDOUBLE","GetDOUBLE","GetDOUBLE method [Windows Management Instrumentation]","GetDOUBLE method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getdouble","instance/CInstance::GetDOUBLE","wmi.cinstance_getdouble"]
old-location: wmi\cinstance_getdouble.htm
tech.root: wmi
ms.assetid: 39360e69-0d54-4b1f-8de8-0abf81e9238b
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetDOUBLE method, CInstance.GetDOUBLE, CInstance::GetDOUBLE, GetDOUBLE, GetDOUBLE method [Windows Management Instrumentation], GetDOUBLE method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getdouble, instance/CInstance::GetDOUBLE, wmi.cinstance_getdouble
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
 - CInstance::GetDOUBLE
 - instance/CInstance::GetDOUBLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetDOUBLE
---

# CInstance::GetDOUBLE


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetDOUBLE</b> method retrieves a <b>DOUBLE</b> property.

## -parameters

### -param name

Name of the <b>DOUBLE</b> property retrieved.

### -param dub [ref]

Buffer to receive the <b>DOUBLE</b> property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a <b>DOUBLE</b>-compatible type or a property that does not exist. More information is available in the log file, Framework.log.