---
UID: NF:instance.CInstance.SetCHString(LPCWSTR,LPCSTR)
title: CInstance::SetCHString(LPCWSTR,LPCSTR) (instance.h)
description: The SetCHString(LPCWSTR, LPCSTR) method sets a string property.
helpviewer_keywords: ["?SetCHString@CInstance@@QAE_NPBG0@Z","?SetCHString@CInstance@@QAE_NPBGPBD@Z","?SetCHString@CInstance@@QEAA_NPEBG0@Z","?SetCHString@CInstance@@QEAA_NPEBGPEBD@Z","CInstance interface [Windows Management Instrumentation]","SetCHString method","CInstance.SetCHString","CInstance.SetCHString(LPCWSTR","LPCSTR)","CInstance::SetCHString","CInstance::SetCHString(LPCWSTR","LPCSTR)","SetCHString","SetCHString method [Windows Management Instrumentation]","SetCHString method [Windows Management Instrumentation]","CInstance interface","instance/CInstance::SetCHString","wmi.cinstance_setchstring_lpcwstr__lpcstr_"]
old-location: wmi\cinstance_setchstring_lpcwstr__lpcstr_.htm
tech.root: wmi
ms.assetid: a5a7a7ab-d187-4eff-a2b9-bd87229c83d1
ms.date: 12/05/2018
ms.keywords: ?SetCHString@CInstance@@QAE_NPBG0@Z, ?SetCHString@CInstance@@QAE_NPBGPBD@Z, ?SetCHString@CInstance@@QEAA_NPEBG0@Z, ?SetCHString@CInstance@@QEAA_NPEBGPEBD@Z, CInstance interface [Windows Management Instrumentation],SetCHString method, CInstance.SetCHString, CInstance.SetCHString(LPCWSTR,LPCSTR), CInstance::SetCHString, CInstance::SetCHString(LPCWSTR,LPCSTR), SetCHString, SetCHString method [Windows Management Instrumentation], SetCHString method [Windows Management Instrumentation],CInstance interface, instance/CInstance::SetCHString, wmi.cinstance_setchstring_lpcwstr__lpcstr_
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
 - CInstance::SetCHString
 - instance/CInstance::SetCHString
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
 - CInstance.SetCHString
 - ?SetCHString@CInstance@@QAE_NPBG0@Z
 - ?SetCHString@CInstance@@QAE_NPBGPBD@Z
 - ?SetCHString@CInstance@@QEAA_NPEBG0@Z
 - ?SetCHString@CInstance@@QEAA_NPEBGPEBD@Z
---

# CInstance::SetCHString(LPCWSTR,LPCSTR)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>SetCHString(LPCWSTR, LPCSTR)</b> method sets a string property.

## -parameters

### -param name

Name of the string property that is set.

### -param str

Value assigned to the string property.

## -returns

Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to set a nonexistent or non-string property.  More information is available in the log file, Framework.log.

## -see-also

<a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>



<a href="/windows/desktop/WmiSdk/cinstance-setchstring">CInstance::SetCHString</a>