---
UID: NF:instance.CInstance.SetCharSplat(LPCWSTR,DWORD)
title: CInstance::SetCharSplat(LPCWSTR,DWORD)
author: windows-sdk-content
description: The SetCharSplat(LPCWSTR, DWORD) method sets a string.
old-location: wmi\cinstance_setcharsplat_lpcwstr__dword_.htm
tech.root: WmiSdk
ms.assetid: 92dd4dc6-9a2c-44f4-b4b1-b8663dc021b0
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetCharSplat method, CInstance.SetCharSplat, CInstance.SetCharSplat(LPCWSTR,DWORD), CInstance::SetCharSplat, CInstance::SetCharSplat(LPCWSTR,DWORD), SetCharSplat, SetCharSplat method [Windows Management Instrumentation], SetCharSplat method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetCharSplat, wmi.cinstance_setcharsplat_lpcwstr__dword_
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
 - CInstance.SetCharSplat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CInstance::SetCharSplat(LPCWSTR,DWORD)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
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




<a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>



<a href="https://msdn.microsoft.com/7f59a2ea-3513-4a14-ac1a-62ed833d7192">CInstance::SetCharSplat</a>
 

 

