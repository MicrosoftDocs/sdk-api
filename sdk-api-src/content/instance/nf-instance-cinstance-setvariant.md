---
UID: NF:instance.CInstance.SetVariant
title: CInstance::SetVariant method
author: windows-driver-content
description: The SetVariant method sets a VARIANT property.
old-location: wmi\cinstance_setvariant.htm
old-project: WmiSdk
ms.assetid: 45201e64-2ecc-4a18-9f41-2392dfe50caf
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: "?SetVariant@CInstance@@QAE_NPBGABUtagVARIANT@@@Z, CInstance, CInstance interface [Windows Management Instrumentation], SetVariant method, CInstance::SetVariant, SetVariant method [Windows Management Instrumentation], SetVariant method [Windows Management Instrumentation], CInstance interface, SetVariant,CInstance.SetVariant, _hmm_cinstance_setvariant, instance/CInstance::SetVariant, wmi.cinstance_setvariant"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TrustLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CInstance.SetVariant
-	?SetVariant@CInstance@@QAE_NPBGABUtagVARIANT@@@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::SetVariant method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetVariant</b> method sets a <b>VARIANT</b> property.


## -parameters




### -param name

Name of the <b>VARIANT</b> property that is set.


### -param variant [ref]

Value assigned to the <b>VARIANT</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if the supplied variant type is not correct for the property being set.  <b>SetVariant</b> also returns <b>FALSE</b> if an attempt is made to set a nonexistent property. More information is available in the log file, Framework.log.



