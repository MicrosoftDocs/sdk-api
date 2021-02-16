---
UID: NF:instance.CInstance.SetWORD
title: CInstance::SetWORD (instance.h)
description: The SetWORD method sets a WORD property.
helpviewer_keywords: ["?SetWORD@CInstance@@QAE_NPBGG@Z","?SetWORD@CInstance@@QEAA_NPEBGG@Z","CInstance interface [Windows Management Instrumentation]","SetWORD method","CInstance.SetWORD","CInstance::SetWORD","SetWORD","SetWORD method [Windows Management Instrumentation]","SetWORD method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setword","instance/CInstance::SetWORD","wmi.cinstance_setword"]
old-location: wmi\cinstance_setword.htm
tech.root: wmi
ms.assetid: e58b98d9-56c2-4e92-90ee-c9ff4fae9f8f
ms.date: 12/05/2018
ms.keywords: ?SetWORD@CInstance@@QAE_NPBGG@Z, ?SetWORD@CInstance@@QEAA_NPEBGG@Z, CInstance interface [Windows Management Instrumentation],SetWORD method, CInstance.SetWORD, CInstance::SetWORD, SetWORD, SetWORD method [Windows Management Instrumentation], SetWORD method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setword, instance/CInstance::SetWORD, wmi.cinstance_setword
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
 - CInstance::SetWORD
 - instance/CInstance::SetWORD
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
 - CInstance.SetWORD
 - ?SetWORD@CInstance@@QAE_NPBGG@Z
 - ?SetWORD@CInstance@@QEAA_NPEBGG@Z
---

# CInstance::SetWORD


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetWORD</b> method sets a <b>WORD</b> property.

## -parameters

### -param name

Name of the <b>WORD</b> property that is set.

### -param w

Value assigned to the <b>WORD</b> property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-<b>WORD</b> property. More information is available in the log file, Framework.log.