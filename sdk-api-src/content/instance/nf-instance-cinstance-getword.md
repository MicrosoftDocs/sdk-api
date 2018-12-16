---
UID: NF:instance.CInstance.GetWORD
title: CInstance::GetWORD
author: windows-sdk-content
description: The GetWORD method retrieves a WORD property.
old-location: wmi\cinstance_getword.htm
tech.root: WmiSdk
ms.assetid: 511e4ce9-33e3-4c64-8016-05dd5630970f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetWORD method, CInstance.GetWORD, CInstance::GetWORD, GetWORD, GetWORD method [Windows Management Instrumentation], GetWORD method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getword, instance/CInstance::GetWORD, wmi.cinstance_getword
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
 - CInstance.GetWORD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance::GetWORD


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetWORD</b> method retrieves a <b>WORD</b> property.


## -parameters




### -param name

Name of the <b>WORD</b> property retrieved.


### -param w [ref]

Buffer that receives the <b>WORD</b> property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a type that is <b>WORD</b>-compatible or a property that does not exist. More information is available in the log file, Framework.log.



