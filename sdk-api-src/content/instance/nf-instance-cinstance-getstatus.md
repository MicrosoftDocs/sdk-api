---
UID: NF:instance.CInstance.GetStatus
title: CInstance::GetStatus (instance.h)
description: The GetStatus method determines whether a property exists and, if so, determines its type.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","GetStatus method","CInstance.GetStatus","CInstance::GetStatus","GetStatus","GetStatus method [Windows Management Instrumentation]","GetStatus method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getstatus","instance/CInstance::GetStatus","wmi.cinstance_getstatus"]
old-location: wmi\cinstance_getstatus.htm
tech.root: wmi
ms.assetid: 355386c5-7cd2-46de-8696-a83bd3f96cc5
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetStatus method, CInstance.GetStatus, CInstance::GetStatus, GetStatus, GetStatus method [Windows Management Instrumentation], GetStatus method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getstatus, instance/CInstance::GetStatus, wmi.cinstance_getstatus
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
 - CInstance::GetStatus
 - instance/CInstance::GetStatus
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
 - CInstance.GetStatus
---

# CInstance::GetStatus


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetStatus</b> method determines whether a property exists and, if so, determines its type.

## -parameters

### -param name

Name of the property to verify.

### -param a_Exists [ref]

<b>TRUE</b> if property exists and <b>FALSE</b> if the property does not exist.

### -param a_VarType

Type of property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> otherwise.