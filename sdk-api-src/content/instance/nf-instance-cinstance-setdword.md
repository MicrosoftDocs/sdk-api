---
UID: NF:instance.CInstance.SetDWORD
title: CInstance::SetDWORD (instance.h)
description: The SetDWORD method sets a DWORD property.
helpviewer_keywords: ["?SetDWORD@CInstance@@QAE_NPBGK@Z","?SetDWORD@CInstance@@QEAA_NPEBGK@Z","CInstance interface [Windows Management Instrumentation]","SetDWORD method","CInstance.SetDWORD","CInstance::SetDWORD","SetDWORD","SetDWORD method [Windows Management Instrumentation]","SetDWORD method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setdword","instance/CInstance::SetDWORD","wmi.cinstance_setdword"]
old-location: wmi\cinstance_setdword.htm
tech.root: wmi
ms.assetid: 06b2ab13-b42d-4dfe-83f2-ecc526977b92
ms.date: 12/05/2018
ms.keywords: ?SetDWORD@CInstance@@QAE_NPBGK@Z, ?SetDWORD@CInstance@@QEAA_NPEBGK@Z, CInstance interface [Windows Management Instrumentation],SetDWORD method, CInstance.SetDWORD, CInstance::SetDWORD, SetDWORD, SetDWORD method [Windows Management Instrumentation], SetDWORD method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setdword, instance/CInstance::SetDWORD, wmi.cinstance_setdword
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
 - CInstance::SetDWORD
 - instance/CInstance::SetDWORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.SetDWORD
 - ?SetDWORD@CInstance@@QAE_NPBGK@Z
 - ?SetDWORD@CInstance@@QEAA_NPEBGK@Z
---

# CInstance::SetDWORD


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetDWORD</b> method sets a <b>DWORD</b> property.

## -parameters

### -param name

Name of the <b>DWORD</b> property that is set.

### -param d

Value assigned to the <b>DWORD</b> property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-<b>DWORD</b> property. More information is available in the log file, Framework.log.