---
UID: NF:instance.CInstance.SetDOUBLE
title: CInstance::SetDOUBLE
author: windows-sdk-content
description: CInstance::SetDOUBLE method
old-location: wmi\cinstance_setdouble.htm
tech.root: WmiSdk
ms.assetid: 5b6e2dcf-6feb-454a-a56a-79ae1506b4f9
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetDOUBLE method, CInstance.SetDOUBLE, CInstance::SetDOUBLE, SetDOUBLE, SetDOUBLE method [Windows Management Instrumentation], SetDOUBLE method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setdouble, instance/CInstance::SetDOUBLE, wmi.cinstance_setdouble
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.SetDOUBLE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- instance.h
: 
- CInstance.SetDOUBLE
: 
---

# CInstance::SetDOUBLE


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]


## -parameters




### -param name

Name of the <b>DOUBLE</b> property that is set.


### -param dub

TBD




#### - d

Value assigned to the <b>DOUBLE</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-<b>DOUBLE</b> property. More information is available in the log file, Framework.log.



