---
UID: NF:instance.CInstance.SetNull
title: CInstance::SetNull (instance.h)
description: The SetNull method sets a property to NULL.
helpviewer_keywords: ["?SetNull@CInstance@@QAE_NPBG@Z","CInstance interface [Windows Management Instrumentation]","SetNull method","CInstance.SetNull","CInstance::SetNull","SetNull","SetNull method [Windows Management Instrumentation]","SetNull method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setnull","instance/CInstance::SetNull","wmi.cinstance_setnull"]
old-location: wmi\cinstance_setnull.htm
tech.root: wmi
ms.assetid: 4157275a-cf71-4aca-ae86-0ae0b0e7fda7
ms.date: 12/05/2018
ms.keywords: ?SetNull@CInstance@@QAE_NPBG@Z, CInstance interface [Windows Management Instrumentation],SetNull method, CInstance.SetNull, CInstance::SetNull, SetNull, SetNull method [Windows Management Instrumentation], SetNull method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setnull, instance/CInstance::SetNull, wmi.cinstance_setnull
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
 - CInstance::SetNull
 - instance/CInstance::SetNull
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
 - CInstance.SetNull
 - ?SetNull@CInstance@@QAE_NPBG@Z
---

# CInstance::SetNull


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetNull</b> method sets a property to <b>NULL</b>.

## -parameters

### -param name

Name of the property to set to <b>NULL</b>.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent property. More information is available in the log file, Framework.log.