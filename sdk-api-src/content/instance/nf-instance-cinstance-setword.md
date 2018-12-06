---
UID: NF:instance.CInstance.SetWORD
title: CInstance::SetWORD
author: windows-sdk-content
description: The SetWORD method sets a WORD property.
old-location: wmi\cinstance_setword.htm
tech.root: WmiSdk
ms.assetid: e58b98d9-56c2-4e92-90ee-c9ff4fae9f8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "?SetWORD@CInstance@@QAE_NPBGG@Z, ?SetWORD@CInstance@@QEAA_NPEBGG@Z, CInstance interface [Windows Management Instrumentation],SetWORD method, CInstance.SetWORD, CInstance::SetWORD, SetWORD, SetWORD method [Windows Management Instrumentation], SetWORD method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_setword, instance/CInstance::SetWORD, wmi.cinstance_setword"
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
 - CInstance.SetWORD
 - ?SetWORD@CInstance@@QAE_NPBGG@Z
 - ?SetWORD@CInstance@@QEAA_NPEBGG@Z
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance::SetWORD


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetWORD</b> method sets a <b>WORD</b> property.


## -parameters




### -param name

Name of the <b>WORD</b> property that is set.


### -param w

Value assigned to the <b>WORD</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-<b>WORD</b> property. More information is available in the log file, Framework.log.



