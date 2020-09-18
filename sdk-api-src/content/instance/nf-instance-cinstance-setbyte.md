---
UID: NF:instance.CInstance.SetByte
title: CInstance::SetByte (instance.h)
description: The SetByte method sets a BYTE property.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","SetByte method","CInstance.SetByte","CInstance::SetByte","SetByte","SetByte method [Windows Management Instrumentation]","SetByte method [Windows Management Instrumentation]","CInstance interface","_hmm_cinstance_setbyte","instance/CInstance::SetByte","wmi.cinstance_setbyte"]
old-location: wmi\cinstance_setbyte.htm
tech.root: wmi
ms.assetid: d6ecbada-4eb6-40ad-9e59-ba77fd3b883a
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetByte method, CInstance.SetByte, CInstance::SetByte, SetByte, SetByte method [Windows Management Instrumentation], SetByte method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setbyte, instance/CInstance::SetByte, wmi.cinstance_setbyte
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
 - CInstance::SetByte
 - instance/CInstance::SetByte
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
 - CInstance.SetByte
---

# CInstance::SetByte


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetByte</b> method sets a <b>BYTE</b> property.

## -parameters

### -param name

Name of the <b>BYTE</b> property that is set.

### -param b

Value assigned to the <b>BYTE</b> property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not <b>BYTE</b> compatible. More information is available in the log file, Framework.log.