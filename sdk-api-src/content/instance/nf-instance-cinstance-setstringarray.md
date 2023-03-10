---
UID: NF:instance.CInstance.SetStringArray
title: CInstance::SetStringArray (instance.h)
description: The SetStringArray method sets a property that represents an array of strings.
helpviewer_keywords: ["?SetStringArray@CInstance@@QAE_NPBGABUtagSAFEARRAY@@@Z","?SetStringArray@CInstance@@QEAA_NPEBGAEBUtagSAFEARRAY@@@Z","CInstance interface [Windows Management Instrumentation]","SetStringArray method","CInstance.SetStringArray","CInstance::SetStringArray","SetStringArray","SetStringArray method [Windows Management Instrumentation]","SetStringArray method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setstringarray","instance/CInstance::SetStringArray","wmi.cinstance_setstringarray"]
old-location: wmi\cinstance_setstringarray.htm
tech.root: wmi
ms.assetid: dcd1e108-4914-43ea-aa41-d38d38e8954a
ms.date: 12/05/2018
ms.keywords: ?SetStringArray@CInstance@@QAE_NPBGABUtagSAFEARRAY@@@Z, ?SetStringArray@CInstance@@QEAA_NPEBGAEBUtagSAFEARRAY@@@Z, CInstance interface [Windows Management Instrumentation],SetStringArray method, CInstance.SetStringArray, CInstance::SetStringArray, SetStringArray, SetStringArray method [Windows Management Instrumentation], SetStringArray method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setstringarray, instance/CInstance::SetStringArray, wmi.cinstance_setstringarray
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
 - CInstance::SetStringArray
 - instance/CInstance::SetStringArray
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
 - CInstance.SetStringArray
 - ?SetStringArray@CInstance@@QAE_NPBGABUtagSAFEARRAY@@@Z
 - ?SetStringArray@CInstance@@QEAA_NPEBGAEBUtagSAFEARRAY@@@Z
---

# CInstance::SetStringArray


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetStringArray</b> method sets a property that represents an array of strings.

## -parameters

### -param name

Name of the property that is set to an array of strings.

### -param strArray [ref]

Value assigned to the array of strings.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not an array of strings. More information is available in the log file, Framework.log.