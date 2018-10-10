---
UID: NF:instance.CInstance.SetDateTime
title: CInstance::SetDateTime
author: windows-sdk-content
description: The SetDateTime method sets a datetime property.
old-location: wmi\cinstance_setdatetime.htm
tech.root: WmiSdk
ms.assetid: 728ad7d3-f56d-472e-976d-59d8598f3bad
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "?SetDateTime@CInstance@@QAE_NPBGABVWBEMTime@@@Z, ?SetDateTime@CInstance@@QEAA_NPEBGAEBVWBEMTime@@@Z, CInstance interface [Windows Management Instrumentation],SetDateTime method, CInstance.SetDateTime, CInstance::SetDateTime, SetDateTime, SetDateTime method [Windows Management Instrumentation], SetDateTime method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setdatetime, instance/CInstance::SetDateTime, wmi.cinstance_setdatetime"
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
 - CInstance.SetDateTime
 - ?SetDateTime@CInstance@@QAE_NPBGABVWBEMTime@@@Z
 - ?SetDateTime@CInstance@@QEAA_NPEBGAEBVWBEMTime@@@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance::SetDateTime


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetDateTime</b> method sets a datetime property.


## -parameters




### -param name

Name of the datetime property that is set.


### -param wbemtime [ref]

Value assigned to the datetime property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-datetime property. More information is available in the log file, Framework.log.

<div class="alert"><b>Note</b>  The <i>wbemtime</i> parameter is converted to local time, and any arbitrary offsets are lost.</div>
<div> </div>


