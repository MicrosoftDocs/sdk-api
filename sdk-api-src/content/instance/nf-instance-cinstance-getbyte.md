---
UID: NF:instance.CInstance.GetByte
title: CInstance::GetByte (instance.h)
description: The GetByte method retrieves a BYTE-compatible property.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","GetByte method","CInstance.GetByte","CInstance::GetByte","GetByte","GetByte method [Windows Management Instrumentation]","GetByte method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_getbyte","instance/CInstance::GetByte","wmi.cinstance_getbyte"]
old-location: wmi\cinstance_getbyte.htm
tech.root: wmi
ms.assetid: a84b2de4-453d-4f69-8bac-df361180bc10
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetByte method, CInstance.GetByte, CInstance::GetByte, GetByte, GetByte method [Windows Management Instrumentation], GetByte method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getbyte, instance/CInstance::GetByte, wmi.cinstance_getbyte
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
 - CInstance::GetByte
 - instance/CInstance::GetByte
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
 - CInstance.GetByte
---

# CInstance::GetByte


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetByte</b> method retrieves a <b>BYTE</b>-compatible property.

## -parameters

### -param name

Name of property retrieved.

### -param b [ref]

Buffer to receive the <b>BYTE</b>-compatible property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not <b>BYTE</b>-compatible or a property that does not exist. More information is available in the log file, Framework.log.