---
UID: NF:instance.CInstance.SetWBEMINT16
title: CInstance::SetWBEMINT16
author: windows-sdk-content
description: The SetWBEMINT16 method sets a 16-bit integer property.
old-location: wmi\cinstance_setwbemint16.htm
tech.root: WmiSdk
ms.assetid: a39d3885-6344-4c05-8eea-da3f33fb998e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "?SetWBEMINT16@CInstance@@QAE_NPBGABF@Z, ?SetWBEMINT16@CInstance@@QEAA_NPEBGAEBF@Z, CInstance interface [Windows Management Instrumentation],SetWBEMINT16 method, CInstance.SetWBEMINT16, CInstance::SetWBEMINT16, SetWBEMINT16, SetWBEMINT16 method [Windows Management Instrumentation], SetWBEMINT16 method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setwbemint16, instance/CInstance::SetWBEMINT16, wmi.cinstance_setwbemint16"
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
 - CInstance.SetWBEMINT16
 - ?SetWBEMINT16@CInstance@@QAE_NPBGABF@Z
 - ?SetWBEMINT16@CInstance@@QEAA_NPEBGAEBF@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance::SetWBEMINT16


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetWBEMINT16</b> method sets a 16-bit integer property.


## -parameters




### -param name

Name of the 16-bit integer property that is set.


### -param wbemint16 [ref]

Value assigned to the 16-bit integer property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent property or a property that is not a 16-bit integer. More information is available in the log file, Framework.log.



