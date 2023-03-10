---
UID: NF:instance.CInstance.SetWCHARSplat
title: CInstance::SetWCHARSplat (instance.h)
description: The SetWCHARSplat method sets a string property.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","SetWCHARSplat method","CInstance.SetWCHARSplat","CInstance::SetWCHARSplat","SetWCHARSplat","SetWCHARSplat method [Windows Management Instrumentation]","SetWCHARSplat method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setwcharsplat","instance/CInstance::SetWCHARSplat","wmi.cinstance_setwcharsplat"]
old-location: wmi\cinstance_setwcharsplat.htm
tech.root: wmi
ms.assetid: 3c565630-3626-4d60-9bd2-74c2218bec11
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetWCHARSplat method, CInstance.SetWCHARSplat, CInstance::SetWCHARSplat, SetWCHARSplat, SetWCHARSplat method [Windows Management Instrumentation], SetWCHARSplat method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setwcharsplat, instance/CInstance::SetWCHARSplat, wmi.cinstance_setwcharsplat
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
 - CInstance::SetWCHARSplat
 - instance/CInstance::SetWCHARSplat
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
 - CInstance.SetWCHARSplat
---

# CInstance::SetWCHARSplat


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetWCHARSplat</b> method sets a string property.

## -parameters

### -param name

Name of the string property to be modified.

### -param pStr

Pointer to the Unicode string.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-string property. More information is available in the log file, Framework.log.