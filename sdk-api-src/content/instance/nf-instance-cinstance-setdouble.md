---
UID: NF:instance.CInstance.SetDOUBLE
title: CInstance::SetDOUBLE (instance.h)
description: CInstance::SetDOUBLE method
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","SetDOUBLE method","CInstance.SetDOUBLE","CInstance::SetDOUBLE","SetDOUBLE","SetDOUBLE method [Windows Management Instrumentation]","SetDOUBLE method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setdouble","instance/CInstance::SetDOUBLE","wmi.cinstance_setdouble"]
old-location: wmi\cinstance_setdouble.htm
tech.root: wmi
ms.assetid: 5b6e2dcf-6feb-454a-a56a-79ae1506b4f9
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetDOUBLE method, CInstance.SetDOUBLE, CInstance::SetDOUBLE, SetDOUBLE, SetDOUBLE method [Windows Management Instrumentation], SetDOUBLE method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setdouble, instance/CInstance::SetDOUBLE, wmi.cinstance_setdouble
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
 - CInstance::SetDOUBLE
 - instance/CInstance::SetDOUBLE
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
 - CInstance.SetDOUBLE
---

# CInstance::SetDOUBLE


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

## -parameters

### -param name

Name of the <b>DOUBLE</b> property that is set.

### -param dub

Value assigned to the <b>DOUBLE</b> property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-<b>DOUBLE</b> property. More information is available in the log file, Framework.log.