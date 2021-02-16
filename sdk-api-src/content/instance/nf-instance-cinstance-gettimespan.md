---
UID: NF:instance.CInstance.GetTimeSpan
title: CInstance::GetTimeSpan (instance.h)
description: The GetTimeSpan method retrieves a property that represents a WMI time span.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","GetTimeSpan method","CInstance.GetTimeSpan","CInstance::GetTimeSpan","GetTimeSpan","GetTimeSpan method [Windows Management Instrumentation]","GetTimeSpan method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_gettimespan","instance/CInstance::GetTimeSpan","wmi.cinstance_gettimespan"]
old-location: wmi\cinstance_gettimespan.htm
tech.root: wmi
ms.assetid: b14c7a62-579b-4a96-b018-c62918c9c35e
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetTimeSpan method, CInstance.GetTimeSpan, CInstance::GetTimeSpan, GetTimeSpan, GetTimeSpan method [Windows Management Instrumentation], GetTimeSpan method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_gettimespan, instance/CInstance::GetTimeSpan, wmi.cinstance_gettimespan
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
 - CInstance::GetTimeSpan
 - instance/CInstance::GetTimeSpan
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
 - CInstance.GetTimeSpan
---

# CInstance::GetTimeSpan


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetTimeSpan</b> method retrieves a property that represents a WMI time span.

## -parameters

### -param name

Name of the time span property retrieved.

### -param wbemtimespan [ref]

Buffer to receive the time span property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if the supplied time span type is not valid for the property being returned or an attempt is made to retrieve a nonexistent property. More information is available in the log file, Framework.log.