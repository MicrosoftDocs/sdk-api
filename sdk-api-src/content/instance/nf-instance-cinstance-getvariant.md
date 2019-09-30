---
UID: NF:instance.CInstance.GetVariant
title: CInstance::GetVariant (instance.h)
author: windows-sdk-content
description: The GetVariant method retrieves a VARIANT property.
old-location: wmi\cinstance_getvariant.htm
tech.root: WmiSdk
ms.assetid: 84160043-bb63-422b-99be-3f55df4c15be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "?GetVariant@CInstance@@QBE_NPBGAAUtagVARIANT@@@Z, CInstance interface [Windows Management Instrumentation],GetVariant method, CInstance.GetVariant, CInstance::GetVariant, GetVariant, GetVariant method [Windows Management Instrumentation], GetVariant method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getvariant, instance/CInstance::GetVariant, wmi.cinstance_getvariant"
ms.topic: method
f1_keywords: 
 - "instance/CInstance.GetVariant"
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
 - CInstance.GetVariant
 - ?GetVariant@CInstance@@QBE_NPBGAAUtagVARIANT@@@Z
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CInstance::GetVariant


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetVariant</b> method retrieves a <b>VARIANT</b> property.


## -parameters




### -param name

Name of the <b>VARIANT</b> property retrieved.


### -param variant [ref]

Buffer to receive the <b>VARIANT</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a nonexistent property or a property with an incompatible data type. More information is available in the log file, Framework.log.



