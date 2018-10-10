---
UID: NF:instance.CInstance.SetDWORD
title: CInstance::SetDWORD
author: windows-sdk-content
description: The SetDWORD method sets a DWORD property.
old-location: wmi\cinstance_setdword.htm
tech.root: WmiSdk
ms.assetid: 06b2ab13-b42d-4dfe-83f2-ecc526977b92
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: "?SetDWORD@CInstance@@QAE_NPBGK@Z, ?SetDWORD@CInstance@@QEAA_NPEBGK@Z, CInstance interface [Windows Management Instrumentation],SetDWORD method, CInstance.SetDWORD, CInstance::SetDWORD, SetDWORD, SetDWORD method [Windows Management Instrumentation], SetDWORD method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setdword, instance/CInstance::SetDWORD, wmi.cinstance_setdword"
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
 - CInstance.SetDWORD
 - ?SetDWORD@CInstance@@QAE_NPBGK@Z
 - ?SetDWORD@CInstance@@QEAA_NPEBGK@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance::SetDWORD


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetDWORD</b> method sets a <b>DWORD</b> property.


## -parameters




### -param name

Name of the <b>DWORD</b> property that is set.


### -param d

Value assigned to the <b>DWORD</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-<b>DWORD</b> property. More information is available in the log file, Framework.log.



