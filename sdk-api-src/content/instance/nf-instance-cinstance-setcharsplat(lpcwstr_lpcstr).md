---
UID: NF:instance.CInstance.SetCharSplat(LPCWSTR,LPCSTR)
title: CInstance::SetCharSplat(LPCWSTR,LPCSTR) (instance.h)
description: The SetCharSplat(LPCWSTR, LPCSTR) method sets a string property.
helpviewer_keywords: ["CInstance interface [Windows Management Instrumentation]","SetCharSplat method","CInstance.SetCharSplat","CInstance.SetCharSplat(LPCWSTR","LPCSTR)","CInstance::SetCharSplat","CInstance::SetCharSplat(LPCWSTR","LPCSTR)","SetCharSplat","SetCharSplat method [Windows Management Instrumentation]","SetCharSplat method [Windows Management Instrumentation]","CInstance interface","instance/CInstance::SetCharSplat","wmi.cinstance_setcharsplat_lpcwstr__lpcstr_"]
old-location: wmi\cinstance_setcharsplat_lpcwstr__lpcstr_.htm
tech.root: wmi
ms.assetid: cdd54a63-749e-47bb-8c92-2678577d8096
ms.date: 12/05/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],SetCharSplat method, CInstance.SetCharSplat, CInstance.SetCharSplat(LPCWSTR,LPCSTR), CInstance::SetCharSplat, CInstance::SetCharSplat(LPCWSTR,LPCSTR), SetCharSplat, SetCharSplat method [Windows Management Instrumentation], SetCharSplat method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetCharSplat, wmi.cinstance_setcharsplat_lpcwstr__lpcstr_
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CInstance::SetCharSplat
 - instance/CInstance::SetCharSplat
dev_langs:
 - c++
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
---

# CInstance::SetCharSplat(LPCWSTR,LPCSTR)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetCharSplat(LPCWSTR, LPCSTR)</b> method sets a string property.

## -parameters

### -param name

Name of the string property that is set.

### -param pStr

Pointer to the new string value.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-string property.  More information is available in the log file, Framework.log.

## -see-also

<a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>



<a href="/windows/desktop/WmiSdk/cinstance-setcharsplat">CInstance::SetCharSplat</a>