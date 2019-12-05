---
UID: NF:instance.CInstance.SetVariant
title: CInstance::SetVariant (instance.h)
description: The SetVariant method sets a VARIANT property.
old-location: wmi\cinstance_setvariant.htm
tech.root: WmiSdk
ms.assetid: 45201e64-2ecc-4a18-9f41-2392dfe50caf
ms.date: 12/05/2018
ms.keywords: ?SetVariant@CInstance@@QAE_NPBGABUtagVARIANT@@@Z, CInstance interface [Windows Management Instrumentation],SetVariant method, CInstance.SetVariant, CInstance::SetVariant, SetVariant, SetVariant method [Windows Management Instrumentation], SetVariant method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setvariant, instance/CInstance::SetVariant, wmi.cinstance_setvariant
ms.topic: method
f1_keywords:
- instance/CInstance.SetVariant
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- CInstance.SetVariant
- ?SetVariant@CInstance@@QAE_NPBGABUtagVARIANT@@@Z
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CInstance::SetVariant


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetVariant</b> method sets a <b>VARIANT</b> property.


## -parameters




### -param name

Name of the <b>VARIANT</b> property that is set.


### -param variant [ref]

Value assigned to the <b>VARIANT</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if the supplied variant type is not correct for the property being set.  <b>SetVariant</b> also returns <b>FALSE</b> if an attempt is made to set a nonexistent property. More information is available in the log file, Framework.log.



