---
UID: NF:instance.CInstance.SetStringArray
title: CInstance::SetStringArray
author: windows-driver-content
description: The SetStringArray method sets a property that represents an array of strings.
old-location: wmi\cinstance_setstringarray.htm
old-project: WmiSdk
ms.assetid: dcd1e108-4914-43ea-aa41-d38d38e8954a
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: "?SetStringArray@CInstance@@QAE_NPBGABUtagSAFEARRAY@@@Z, ?SetStringArray@CInstance@@QEAA_NPEBGAEBUtagSAFEARRAY@@@Z, CInstance interface [Windows Management Instrumentation],SetStringArray method, CInstance.SetStringArray, CInstance::SetStringArray, SetStringArray, SetStringArray method [Windows Management Instrumentation], SetStringArray method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setstringarray, instance/CInstance::SetStringArray, wmi.cinstance_setstringarray"
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
-	CInstance.SetStringArray
-	?SetStringArray@CInstance@@QAE_NPBGABUtagSAFEARRAY@@@Z
-	?SetStringArray@CInstance@@QEAA_NPEBGAEBUtagSAFEARRAY@@@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::SetStringArray


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetStringArray</b> method sets a property that represents an array of strings.


## -parameters




### -param name

Name of the property that is set to an array of strings.


### -param strArray [ref]

Value assigned to the array of strings.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not an array of strings. More information is available in the log file, Framework.log.



