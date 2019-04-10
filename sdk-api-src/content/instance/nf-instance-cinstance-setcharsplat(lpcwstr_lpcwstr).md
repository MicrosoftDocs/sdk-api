---
UID: NF:instance.CInstance.SetCharSplat(LPCWSTR,LPCWSTR)
title: CInstance::SetCharSplat(LPCWSTR,LPCWSTR) (instance.h)
author: windows-sdk-content
description: The SetCharSplat(LPCWSTR, LPCWSTR) method sets a string property.
old-location: wmi\cinstance_setcharsplat_lpcwstr__lpcwstr_.htm
tech.root: WmiSdk
ms.assetid: 27860c70-9ed5-4744-a643-f3074abe6575
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetCharSplat method, CInstance.SetCharSplat, CInstance.SetCharSplat(LPCWSTR,LPCWSTR), CInstance::SetCharSplat, CInstance::SetCharSplat(LPCWSTR,LPCWSTR), SetCharSplat, SetCharSplat method [Windows Management Instrumentation], SetCharSplat method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetCharSplat, wmi.cinstance_setcharsplat_lpcwstr__lpcwstr_
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

# CInstance::SetCharSplat(LPCWSTR,LPCWSTR)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>SetCharSplat(LPCWSTR, LPCWSTR)</b> method sets a string property.


## -parameters




### -param name

Name of the string property that is set.


### -param pStr

Pointer to the new string value.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-string property.  More information is available in the log file, Framework.log.




## -see-also




<a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>



<a href="https://msdn.microsoft.com/7f59a2ea-3513-4a14-ac1a-62ed833d7192">CInstance::SetCharSplat</a>
 

 

