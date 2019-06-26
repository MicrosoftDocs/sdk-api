---
UID: NF:instance.CInstance.SetCharSplat(LPCWSTR,DWORD)
title: CInstance::SetCharSplat(LPCWSTR,DWORD) (instance.h)
author: windows-sdk-content
description: The SetCharSplat(LPCWSTR, DWORD) method sets a string.
old-location: wmi\cinstance_setcharsplat_lpcwstr__dword_.htm
tech.root: WmiSdk
ms.assetid: 92dd4dc6-9a2c-44f4-b4b1-b8663dc021b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetCharSplat method, CInstance.SetCharSplat, CInstance.SetCharSplat(LPCWSTR,DWORD), CInstance::SetCharSplat, CInstance::SetCharSplat(LPCWSTR,DWORD), SetCharSplat, SetCharSplat method [Windows Management Instrumentation], SetCharSplat method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetCharSplat, wmi.cinstance_setcharsplat_lpcwstr__dword_
ms.topic: method
f1_keywords: 
 - "instance/CInstance.SetCharSplat"
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
 - CInstance.SetCharSplat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CInstance::SetCharSplat(LPCWSTR,DWORD)


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetCharSplat(LPCWSTR, DWORD)</b> method sets a string.


## -parameters




### -param name

Name of the string property that is set.


### -param dwResID

Resource identifier of the new string value.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-string property.  More information is available in the log file, Framework.log.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/cinstance-setcharsplat">CInstance::SetCharSplat</a>
 

 

