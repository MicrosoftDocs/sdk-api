---
UID: NF:instance.CInstance.SetDateTime
title: CInstance::SetDateTime (instance.h)
description: The SetDateTime method sets a datetime property.
helpviewer_keywords: ["?SetDateTime@CInstance@@QAE_NPBGABVWBEMTime@@@Z","?SetDateTime@CInstance@@QEAA_NPEBGAEBVWBEMTime@@@Z","CInstance interface [Windows Management Instrumentation]","SetDateTime method","CInstance.SetDateTime","CInstance::SetDateTime","SetDateTime","SetDateTime method [Windows Management Instrumentation]","SetDateTime method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setdatetime","instance/CInstance::SetDateTime","wmi.cinstance_setdatetime"]
old-location: wmi\cinstance_setdatetime.htm
tech.root: wmi
ms.assetid: 728ad7d3-f56d-472e-976d-59d8598f3bad
ms.date: 12/05/2018
ms.keywords: ?SetDateTime@CInstance@@QAE_NPBGABVWBEMTime@@@Z, ?SetDateTime@CInstance@@QEAA_NPEBGAEBVWBEMTime@@@Z, CInstance interface [Windows Management Instrumentation],SetDateTime method, CInstance.SetDateTime, CInstance::SetDateTime, SetDateTime, SetDateTime method [Windows Management Instrumentation], SetDateTime method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setdatetime, instance/CInstance::SetDateTime, wmi.cinstance_setdatetime
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
 - CInstance::SetDateTime
 - instance/CInstance::SetDateTime
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
 - CInstance.SetDateTime
 - ?SetDateTime@CInstance@@QAE_NPBGABVWBEMTime@@@Z
 - ?SetDateTime@CInstance@@QEAA_NPEBGAEBVWBEMTime@@@Z
---

# CInstance::SetDateTime


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetDateTime</b> method sets a datetime property.

## -parameters

### -param name

Name of the datetime property that is set.

### -param wbemtime [ref]

Value assigned to the datetime property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-datetime property. More information is available in the log file, Framework.log.

<div class="alert"><b>Note</b>  The <i>wbemtime</i> parameter is converted to local time, and any arbitrary offsets are lost.</div>
<div> </div>