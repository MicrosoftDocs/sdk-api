---
UID: NF:instance.CInstance.Setbool
title: CInstance::Setbool (instance.h)
description: The Setbool method sets a Boolean property.
helpviewer_keywords: ["?Setbool@CInstance@@QAE_NPBG_N@Z","?Setbool@CInstance@@QEAA_NPEBG_N@Z","CInstance interface [Windows Management Instrumentation]","Setbool method","CInstance.Setbool","CInstance::Setbool","Setbool","Setbool method [Windows Management Instrumentation]","Setbool method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setbool","instance/CInstance::Setbool","wmi.cinstance_setbool"]
old-location: wmi\cinstance_setbool.htm
tech.root: wmi
ms.assetid: d4ca045d-a018-48a0-a4ea-94d0c8f094a6
ms.date: 12/05/2018
ms.keywords: ?Setbool@CInstance@@QAE_NPBG_N@Z, ?Setbool@CInstance@@QEAA_NPEBG_N@Z, CInstance interface [Windows Management Instrumentation],Setbool method, CInstance.Setbool, CInstance::Setbool, Setbool, Setbool method [Windows Management Instrumentation], Setbool method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setbool, instance/CInstance::Setbool, wmi.cinstance_setbool
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
 - CInstance::Setbool
 - instance/CInstance::Setbool
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
 - CInstance.Setbool
 - ?Setbool@CInstance@@QAE_NPBG_N@Z
 - ?Setbool@CInstance@@QEAA_NPEBG_N@Z
---

# CInstance::Setbool


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Setbool</b> method sets a Boolean property.

## -parameters

### -param name

Name of the Boolean property that is set.

### -param b

Value assigned to the Boolean property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a non-Boolean property or a property that does not exist. More information is available in the log file, Framework.log.